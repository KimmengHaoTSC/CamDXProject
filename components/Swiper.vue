<template>
  <client-only>
    <div ref="swiper" class="swiper mySwiper">
      <div class="swiper-wrapper">
        <div v-for="(item, i) in items" :key="i" class="swiper-slide">
          <v-row>
            <v-col cols="12" align="center">
              <v-img
                :contain="true"
                height="100"
                :src="require('assets/' + item.icon + '.png')"
                rel="preload"
              >
                <template #placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                  >
                   <v-skeleton-loader
                      class="mx-auto"
                      max-width="300"
                      type="card"
                    ></v-skeleton-loader>
                  </v-row>
                </template>
              </v-img>
            </v-col>
            <v-col cols="12" align="center">
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
      freeMode: true,
      centeredSlides: true,
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      lazy: 'true',
      slidesPerView: 3,
      spaceBetween: 40,
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    })
  },
}
</script>

<style>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}
</style>
