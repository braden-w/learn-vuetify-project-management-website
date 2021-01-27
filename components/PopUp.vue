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
        <v-form class="px-3">
          <v-text-field
            v-model="title"
            label="Title"
            prepend-icon="mdi-folder"
          />
          <v-textarea
            v-model="content"
            label="Information"
            prepend-icon="mdi-pencil"
          />
          <v-menu>
            <template #activator="{ on, attrs }">
              <v-text-field
                :value="date"
                label="due date"
                prepend-icon="mdi-calendar"
                @click="on"
              >
              </v-text-field>
            </template>
            <v-date-picker v-model="date" no-title scrollable> </v-date-picker>
          </v-menu>
          <v-btn class="success" @click="submit">Add project</v-btn>
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
    }
  },
  methods: {
    submit() {
      console.log(this.title, this.content)
    },
  },
}
</script>

<style></style>
