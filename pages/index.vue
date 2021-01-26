<template>
  <div class="home">
    <h1>Homepage</h1>
    <v-btn class="pink white--text">Click me</v-btn>
    <v-btn depressed color="pink">Click me</v-btn>
    <v-btn flat color="pink">Click me</v-btn>
    <v-btn depressed class="pink white--text">
      <v-icon left>mdi-email</v-icon>
      <span>Email me</span>
    </v-btn>
    <v-btn small depressed class="pink white--text">
      <v-icon left>mdi-email</v-icon>
      <span>Email me</span>
    </v-btn>
    <v-btn large depressed class="pink white--text">
      <v-icon left>mdi-email</v-icon>
      <span>Email me</span>
      <v-icon right>mdi-email</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  components: {},
}
</script>
