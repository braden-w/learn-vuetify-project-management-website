<template>
  <v-dialog v-model="dialog">
    <template #activator="{ on, attrs }">
      <v-btn color="secondary" dark v-bind="attrs" v-on="on">
        Create Project
      </v-btn>
    </template>
    <v-card>
      <v-card-title>Add New Project</v-card-title>
      <v-card-text>
        <v-form ref="form" class="px-3">
          <v-text-field
            v-model="title"
            label="Title"
            prepend-icon="mdi-folder"
            :rules="inputRules"
          />
          <v-textarea
            v-model="content"
            label="Information"
            prepend-icon="mdi-pencil"
          />
          <v-menu>
            <template #activator="{ on, attrs }">
              <v-text-field
                v-bind="attrs"
                :value="date"
                label="Due Date"
                prepend-icon="mdi-calendar"
                :rules="inputRules"
                v-on="on"
              >
              </v-text-field>
            </template>
            <v-date-picker v-model="date" no-title scrollable> </v-date-picker>
          </v-menu>
          <v-btn class="success" :loading="loading" @click="submit"
            >Add project</v-btn
          >
        </v-form>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      content: '',
      date: '',
      inputRules: [(v) => v.length >= 3 || 'Please fill in required inputs'],
      loading: false,
      dialog=false,
    }
  },
  methods: {
    async submit() {
      if (this.$refs.form.validate()) {
        try {
          this.loading = true
          await this.$fire.firestore.collection('projects').add({
            title: this.title,
            content: this.content,
            due: this.date,
            person: 'Braden',
            status: 'ongoing',
          })
          this.loading = false
          this.dialog=true
          console.log('Success')
        } catch (err) {
          console.error(err)
        }
      }
    },
  },
}
</script>

<style></style>
