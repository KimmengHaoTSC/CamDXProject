<template>
  <v-card class="rounded-0 pa-10" light>
    <v-container>
      <v-col cols="12">
        <div class="text-h3 bold font-weight-medium">
          CamDigiKey, {{ $t('obrPage.maintitle') }}
        </div>
      </v-col>
      <v-col cols="12">
        <div class="text-md">
          {{ $t('obrPage.subtitle') }}
        </div>
      </v-col>
      <v-card color="#C5C5C4" light height="300"></v-card>
      <!-- <br /> -->
      <v-col cols="12">
      <div class="ma-5 text-h3 font-weight-medium text-center">
          {{ $t('obrPage.newfeature.title') }}
      </div>
      </v-col>
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
        title: 'obrPage.newfeature.content1'
      },
      {
        icon: 'camdx_thumbnail',
        title: 'obrPage.newfeature.content2'
      },
      {
        icon: 'camdx_thumbnail',
        title: 'obrPage.newfeature.content3'
      },
      {
        icon: 'camdx_thumbnail',
        title: 'obrPage.newfeature.content4'
      },
    ],
  }),
}
</script>