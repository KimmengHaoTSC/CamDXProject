<template>
  <v-container 
      style="margin-top: 250px;" data-aos="fade-down" 
      data-aos-duration="800">
        <v-list class="listItem" >
          <v-list-item 
            
            v-for="(item, i) in items"
            :key="i" 
            @click="$vuetify.goTo('#' + item.to)"
          >
            <v-list-item-title data-aos="fade-left">{{ $t(item.label) }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-container>


</template>
<script>
export default {
  name: 'ListTabPage',
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
}
</script>