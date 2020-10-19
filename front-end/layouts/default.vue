<template>
  <v-app>
    <appBar />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import appBar from './AppBar'
export default {
  components: {
    appBar
  }
};
</script>

<style>
  a {
    text-decoration: none;
  }
</style>