<template>
  <v-app class="grey lighten-4">
    <v-content><TheNavBar /></v-content>
    <Nuxt />
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
