<template>
  <v-app class="grey lighten-4">
    <v-main class="mx-16">
      <TheNavBar />
      <div class="mx-24"><Nuxt /></div>
    </v-main>
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
