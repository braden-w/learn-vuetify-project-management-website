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
      <span>Email me</span>
      <v-icon right>mdi-email</v-icon>
    </v-btn>
    <v-btn fab depressed class="pink white--text">
      <v-icon>mdi-heart</v-icon>
    </v-btn>
    <v-btn class="hidden-md-and-down">Hidden for middle and lower</v-btn>
  </div>
</template>

<script>
export default {
  components: {},
}
</script>
