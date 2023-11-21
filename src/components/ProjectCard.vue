<template>
  <div class="container" v-on:click="openModale">
    <h3>{{ title }}</h3>
    <img :src="img_URL" class="img" />
  </div>
  <Modale
    v-if="revele"
    :title="title"
    :technologies="technologies"
    :img_URL="img_URL"
    :date_creation="date_creation"
    :github="github"
    v-on:closeModale="closeModale"
  />
</template>

<script setup>
import { ref } from "vue";
import Modale from "./Modale.vue";

defineProps(["title", "technologies", "img_URL", "date_creation", "github"]);

const revele = ref(false);

function openModale() {
  revele.value = true;
}

function closeModale() {
  revele.value = false;
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Cabin&family=Roboto:ital,wght@0,100;1,100&display=swap");
.container {
  width: 500px;
  background-color: #B1C9EF;
  border-radius: 3%;
}

h3 {
  font-family: Cabin;
  text-align: center;
  cursor: pointer;
  text-decoration: underline;
}

.img {
  display: block;
  height: 200px;
  padding-top: 20px;
  margin: auto;
  margin-bottom: 30px;
  cursor: pointer;
}
</style>
