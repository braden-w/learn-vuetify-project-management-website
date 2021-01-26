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
          <v-btn class="success">Add project</v-btn>
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
