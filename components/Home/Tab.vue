<template>
  <v-tabs
    class="white"
    centered
    light
    show-arrows
    :hide-slider="true"
  >
    <v-tab
      v-for="(item, index) in items"
      :key="index"
      class="text-capitalize tabtextSize"
      @click="$vuetify.goTo('#' + item.to, scrollOptions)"
    >
      {{ item.label }}
    </v-tab>
  </v-tabs>
</template>
<script>
import {  mapGetters } from 'vuex'
export default {
  name: 'TabPage',
  data() {
    return {
      isIntersecting: false,
      items: [
        {
          label: 'Overview',
          to: 'overview',
        },
        {
          label: 'Principles',
          to: 'principles',
        },
        {
          label: 'CamDigiKey',
          to: 'camdigikey',
        },
        {
          label: 'Service',
          to: 'service',
        },
        {
          label: 'F.A.Q',
          to: 'faq',
        },
        {
          label: 'Contact',
          to: 'contact',
        },
      ],
    }
  },
  computed: {
    ...mapGetters({scrollOptions: 'scroll/scrollOptions'})
  }
}
</script>
<style>
.tabfont {
  color: black;
}

.v-tab.v-tab--active::before {
  opacity: 0 !important;
}

#custom-tab-items {
  background-color: transparent !important;
}
.tabtextSize {
  font-size: 15px;
}
</style>