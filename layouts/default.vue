<template>
  <v-app class="grey lighten-4">
    <v-content><TheNavBar /> <Nuxt /></v-content>
  </v-app>
</template>

<script>
import TheNavBar from '@/components/TheNavBar'
export default {
  components: {
    TheNavBar,
  },
  data() {
    return {
      title: 'Vuetify.js',
    }
  },
}
</script>
