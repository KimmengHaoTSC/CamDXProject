<template>
  <v-card class="rounded-0 pa-5" light>
    <v-container>
      <v-row>
        <v-col cols="12" md="12" sm="12" xs="12">
          <div class="titleSize">
            {{ $t('homePage.secureserver.title') }}
          </div>
        </v-col>
        <v-col cols="12" md="12" sm="12" xs="12">
          <div class="subtitleSize md-2">
            {{ $t('homePage.secureserver.subtitle') }}
          </div>
        </v-col>
      </v-row>
      <v-row class="d-flex align-center mb-6">
        <!-- <v-col class="d-flex align-center mb-6" data-aos="fade-right"> -->
        <v-col cols="12" md="8" sm="12" xs="12" data-aos="fade-right">
          <v-row v-for="(item, index) in items" :key="index">
            <v-col cols="2" xl="2" md="2" sm="2" xs="2">
              <v-img
                :src="require('assets/point.png')"
                :contain="true"
                max-height="20"
              >
              </v-img>
            </v-col>
            <v-col cols="10" xl="10" md="10" sm="10" xs="10" class="textSize">
              {{ $t(item) }}
            </v-col>
          </v-row>
        </v-col>
        <v-img
            class="img-fluid"
            max-height="400px"
            :contain="true"
            :src="require('assets/secure.png')"
        ></v-img>
      </v-row>
    </v-container>
  </v-card>
</template>
<script>
export default {
  name: 'SecureServerpage',
  data: () => ({
    items: [
      'homePage.secureserver.char1',
      'homePage.secureserver.char2',
      'homePage.secureserver.char3',
      'homePage.secureserver.char4',
      'homePage.secureserver.char5',
    ],
  }),
}
</script>