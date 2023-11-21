<script setup>
import data from "../assets/data/data.json";
import ProjectCard from "../components/ProjectCard.vue";
</script>

<template>
  <body>
    <h1>Projets</h1>
    <div class="container">
      <ProjectCard
        v-for="project in data"
        :title="project.title"
        :technologies="project.technologies"
        :img_URL="project.img"
        :date_creation="project.date_creation"
        :github="project.github"
      />
    </div>
  </body>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Cabin&family=Roboto:ital,wght@0,100;1,100&display=swap");

body {
  width: auto;
  height: 1080px;
}

h1 {
  text-align: center;
  display: block;
  font-family: Cabin;
  text-decoration: underline;
}

.container {
  display: flex;
  column-gap: 50px;
  justify-content: center;
  width: 100%;
  flex-wrap: wrap;
  row-gap: 50px;
  
}
</style>
