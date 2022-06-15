<template>
  <v-app dark>
    <AppBar />
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      class="backgroundTheme fb-btn"
      fab
      dark
      fixed
      depressed
      filled
      bottom
      right
      @click="toTop"
    >
      <v-icon>mdi-arrow-up</v-icon>
    </v-btn>
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import AppBar from '../components/AppBar.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'DefaultLayoutPage',
  components: { AppBar, Footer },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      fab: false,
      fabTab: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 400
      this.fabTab = top > 700
    },
    toTop() {
      this.$vuetify.goTo(0)
    },
  },
}
</script>
<style>
.fb-btn.v-btn {
  border: thin solid #ffffff !important;
}
.v-application {
  font-family: 'Hanuman', cursive !important;
}
.title {
  font-size: large;
}
.subtitle {
  font-size: medium;
}

.listItem {
  background: #26296c !important;
  opacity: 0.98;
}
</style>
