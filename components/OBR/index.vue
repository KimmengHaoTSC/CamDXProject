<template>
  <v-card class="rounded-0 pa-5" light>
    <v-container>
      <v-col cols="12">
        <div class="titleSize text-left">
          CamDigiKey, {{ $t('obrPage.maintitle') }}
        </div>
      </v-col>
      <v-col cols="12">
        <div class="subtitleSize text-left">
          {{ $t('obrPage.subtitle') }}
        </div>
      </v-col>
      <v-card color="#C5C5C4" light height="300"></v-card>
      <!-- <br /> -->
      <v-col cols="12">
      <div class="ma-5 titleSize">
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