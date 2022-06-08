<template>
  <!-- <v-card> -->
    <!-- <v-sheet elevation='6'
      elevate-on-scroll> -->
      <div>
      <v-tabs
      :background-color='tabbgcolor' centered 
      :dark="tabbgcolor=='#16184E'" :light="tabbgcolor=='#FFFFFF'"
      next-icon="mdi-arrow-right-bold-box-outline"
      prev-icon="mdi-arrow-left-bold-box-outline"
      show-arrows >
      <v-col cols="12" align="center">
        <v-btn text
          v-for="(item,index) in items" 
          :key="index" class="text-capitalize"
          @click="$vuetify.goTo('#'+item.to, options)" >
          {{ item.label }}
        </v-btn></v-col>
      </v-tabs>
      <v-tabs-items id="custom-tab-items">
        <v-tab-item value="tabs-1">
        </v-tab-item>
        <v-tab-item value="tabs-2">
        </v-tab-item>
      </v-tabs-items>
      </div>
    <!-- </v-sheet> -->
  <!-- </v-card> -->
</template>
<script>
export default {
  name: 'TabPage',
  props: ["tabbgcolor"],
  data() {
    return {
      items:[
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
  }

}
</script>
<style>
.tabfont {
  color: black
}

#custom-tab-items {
  background-color: transparent !important;
}
</style>