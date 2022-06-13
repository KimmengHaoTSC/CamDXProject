<template>
  <v-card class="pa-5" dark color="#16184E">
    <v-container>
        <div class="text-h3 font-weight-medium text-center pb-5">
          Our Partners
        </div>
          <Swiper :items="items" />
    </v-container>
  </v-card>
</template>
<script>
import Swiper from '../Swiper.vue'
export default {
  name: 'PartnerPage',
  components: { Swiper },
  data: () => ({
    items: [
      {
        icon: 'partner1',
        title: '',
      },
      {
        icon: 'partner2',
        title: '',
      },
      {
        icon: 'partner3',
        title: '',
      },
      {
        icon: 'partner4',
        title: '',
      },
    ],
  }),
}
</script>
<style>
</style>