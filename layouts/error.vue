<template>
  <v-app light>
    <v-container fill-height fluid>
      <v-row align="center">
        <v-col align="center">
          <h1 v-if="error.statusCode === 404">Page not found</h1>
          <h1 v-else>An error occurred</h1>
          <nuxt-link to="/">Home page</nuxt-link>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'EmptyLayout',
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
