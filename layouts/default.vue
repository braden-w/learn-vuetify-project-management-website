<template>
  <v-app>
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
