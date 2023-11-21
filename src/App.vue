<script setup>
import { RouterLink, RouterView } from "vue-router";
import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue"

</script>

<template>
  <body>
      <NavBar />
      <RouterView />
      <Footer />
  </body>
</template>

<style scoped>

body {
  background-color: white;
  padding: 0;
  margin: 0;
}

</style>
