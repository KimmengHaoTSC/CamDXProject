<template>
  <v-app dark>
    <SiteHeader />
    <v-btn v-scroll="onScroll" v-show="fab" class="fb-btn " fab dark fixed depressed filled bottom right color="#16184E" @click="toTop">
        <v-icon>mdi-arrow-up</v-icon>
    </v-btn>
    <v-main>
        <Nuxt />
    </v-main> 
    <Footer />
  </v-app>
</template>

<!-- <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script> -->
<script>
// import AppBar from '../components/AppBar.vue';
import Footer from '../components/Home/Footer.vue';
import SiteHeader from '../components/Home/siteHeader.vue';
// import AOS from "aos";
export default {
    name: "DefaultLayoutPage",
    components: { Footer, SiteHeader },
    created() {
        // AOS.init();
    },
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            fab: false,
            fabTab: false,
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/",
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire",
                },
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: "Vuetify.js",
        };
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
        }
    }
}
</script>
<style>
  .fb-btn.v-btn {
    border: thin solid #ffffff !important;
  }
  .floatAboveEverything {
	z-index: 1000; 
	position: absolute;
}
</style>
