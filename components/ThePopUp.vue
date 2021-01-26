<template>
  <v-dialog v-model="dialog">
    <template #activator="{ on, attrs }">
      <v-btn color="secondary" dark v-bind="attrs" v-on="on">
        Create Project
      </v-btn>
    </template>
    <v-card> Project settings</v-card>
  </v-dialog>
</template>

<script>
export default {}
</script>

<style></style>
