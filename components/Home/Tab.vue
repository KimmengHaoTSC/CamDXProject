<template>
  <v-tabs
    :background-color="tabbgcolor"
    centered
    :dark="tabbgcolor == '#16184E'"
    :light="tabbgcolor == '#FFFFFF'"
    next-icon="mdi-arrow-right-bold-box-outline"
    prev-icon="mdi-arrow-left-bold-box-outline"
    show-arrows
    hide-slider="true"
    align-with-title="false"
    @scroll="handleScroll"
  >
    <v-tab
      v-for="(item, index) in items"
      :key="index"
      class="text-capitalize"
      @click="$vuetify.goTo('#' + item.to, options)"
    >
      {{ item.label }}
    </v-tab>
  </v-tabs>
</template>
<script>
export default {
  name: 'TabPage',
  props: ['tabbgcolor'],
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
  methods: {},
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
</style>