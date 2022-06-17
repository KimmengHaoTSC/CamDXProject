<template>
  <client-only>
    <div ref="swiper" class="swiper mySwiper text-center">
     <div class="swiper-wrapper" >
        <div v-for="(item, i) in items" :key="i" class="swiper-slide pt-5">
          <v-row>
            <v-col cols="12">
              <v-img :contain="true" height="100" :src="require('assets/' + item.icon + '.png')" rel="preload">
                <template #placeholder>
                  <v-row class="fill-height ma-0">
                    <v-skeleton-loader class="mx-auto" max-width="300" type="card"></v-skeleton-loader>
                  </v-row>
                </template>
              </v-img>
            </v-col>
            <v-col cols="12">
              {{ $t(item.title) }}
            </v-col>
          </v-row>
        </div>
      </div>
    </div>
  </client-only>
</template>

<script>
import Swiper from 'swiper/swiper-bundle.min'
import 'swiper/swiper-bundle.min.css'

export default {
  name: 'SwiperPage',
  props: {
    items: {
      type: [],
      default: [],
    },
  },
  async mounted() {
    await this.$nextTick()
    /* eslint-disable no-new */
    new Swiper(this.$refs.swiper, {
      slidesPerView: this.height(this.$vuetify.breakpoint.name) < 300 ? 2 : 3,
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      speed: 1000,
      spaceBetween: 20,
      grabCursor: true,
    })
  },
  methods: {
    height(size) {
      switch (size) {
        case 'xs':
          return 220
        case 'sm':
          return 400
        case 'md':
          return 500
        case 'lg':
          return 600
        case 'xl':
          return 800
      }
    },
  },
}
</script>

<style lang="scss">
.swiper-slide {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;

  &.swiper-slide-active,
  &.swiper-slide-duplicate-active {
    .slide-image {
      transform: scale3d(1, 1, 1);
    }
  }
}

.swiper-wrapper {
  // enough width to have off screen slides partially visible
  // width: 73.8%;
  will-change: transform;
}
</style>
