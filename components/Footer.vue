<template>
  <v-card class="pa-5 backgroundTheme" dark>
    <v-container>
      <v-row class="ma-4 titleSize"> CamDX </v-row>
      <v-col cols="12">
        <v-row class="ma-4 textSize">
          <v-col cols="12" md="5" sm="6" xs="12">
            <v-row class="mb-3"
              >Ministry of Economy and Finance<br />
              Phnom Penh, Cambodia
            </v-row>
            <v-row class="mb-3">{{$t('footer.phone')}} : &nbsp;
              <a href="tel:'`(855) 81 888 296`"> (855) 81 888 296</a></v-row
            >
            <v-row class="mb-3">
            {{$t('footer.email')}} : &nbsp; <a :href="`mailto:camdx@mef.gov.kh`"> camdx@mef.gov.kh </a></v-row>
          </v-col>
          <v-col
            v-if="$route.path === '/' || $route.path == '/kh'"
            cols="12"
            md="3"
            sm="6"
            xs="12"
          >
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#overview')"> CamDX </a>
            </v-row>
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#principles')"> Principles </a>
            </v-row>
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#camdigikey')"> CamDigiKey </a>
            </v-row>
          </v-col>
          <v-col
            v-if="$route.path === '/' || $route.path == '/kh'"
            cols="12"
            md="2"
            sm="6"
            xs="12"
          >
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#service')"> Services </a>
            </v-row>
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#faq')"> F.A.Q </a>
            </v-row>
            <v-row class="mb-5">
              <v-icon>mdi-chevron-right</v-icon>
              <a @click="$vuetify.goTo('#contact')"> Contact Us </a>
            </v-row>
          </v-col>
          <v-col cols="12" md="2" sm="6" xs="12" align="center">
            <v-row class="mb-5 text-left">{{$t('footer.connected')}}</v-row>
            <v-row>
              <v-btn
                text
                href="https://www.facebook.com/CambodiaDX"
                target="_blank"
              >
                <v-icon color="blue" large>mdi-facebook</v-icon>
              </v-btn>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
      <v-divider></v-divider>
      <v-row class="ma-4"  >
        <div class="textSize mb-4">{{ $t('footer.allrightreserve') }}</div>
        <v-spacer></v-spacer>
        <div class="textSize">
          <a href="https://camdx.gov.kh/terms.html">{{ $t('footer.termsofuse') }}</a>
          | 
          <a href="https://camdx.gov.kh/privacy.html">{{ $t('footer.privacypolicy') }}</a>
          </div>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: 'FooterMyPage',
}
</script>
<style scoped>
    a {
        color: white !important;
        text-decoration: none
    }
</style>