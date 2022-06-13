<template>
  <v-card class="rounded-0 pa-10" light>
    <v-container>
      <v-col cols="12">
        <div class="text-h3 bold font-weight-medium">
          CamDigiKey, {{ $t('camAuthenApp') }}
        </div>
      </v-col>
      <v-col cols="12">
        <div class="text-md">
          CamDigiKey is a secure yet easy mobile application to authenticate
          oneself digitally to access to various government digital services
          running through CamDX. Users must register to obtain valid digital
          identity. To login, users simply use the application to scan the QR
          code appeared in the login screen of the government portals. Online
          Business Registration is the first government portal that uses
          CamDigiKey to authenticate the user digital identity.
        </div>
      </v-col>
      <v-card class="ma-10" color="#C5C5C4" light height="300"></v-card>
      <!-- <br /> -->
      <Swiper :items="items"></Swiper>
    </v-container>
  </v-card>
</template>

<script>
import Swiper from '../Swiper.vue'
export default {
  name: 'OBRindex',
  components: {Swiper},
  data: () => ({
    items: [
      {
        icon: 'camdx_thumbnail',
        title: 'Liveness face detection',
      },
      {
        icon: 'camdx_thumbnail',
        title: 'Machine readable zone (MRZ) code reading',
      },
      {
        icon: 'camdx_thumbnail',
        title: 'App-to-app integration',
      },
      {
        icon: 'camdx_thumbnail',
        title: 'Web-to-web integration',
      },
    ],
  }),
}
</script>