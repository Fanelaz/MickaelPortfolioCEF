<template>
  <div class="Navigation">
    <nav>
      <div class="logo">
        <router-link to="/">
          <img class="logotete" src="../assets/imgs/imgcv.jpg" alt="" />
        </router-link>
      </div>
      <ul class="menu">
        <li><router-link to="/">Acceuil</router-link></li>
        <li><router-link to="/projets">Projets</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
};

import { RouterLink, RouterView } from "vue-router";
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Cabin&family=Roboto+Condensed:wght@100&family=Roboto:ital,wght@0,100;1,100&display=swap");


.logo {
  display: flex;
  align-items: center;
  margin-left: 10%;
  padding: 10px;
}
.logo img {
  width: 100px;
  margin-top: 10px;
}

img {
  border-radius: 100%;
}

nav {
  background-color: #395886;
  font-family: Roboto;
  display: flex;
  justify-content: center;
  width: 100%;
}

nav ul {
  display: flex;
  list-style: none;
  text-align: center;
  width: 100%;
  flex-wrap: wrap;
  justify-content: center;
}
nav ul li {
  display: flex;
  align-items: center;
}
nav ul li a {
  display: block;
  padding: 15px;
  font-size: large;
  text-decoration: none;
  color: black;
  font-weight: 800;
  text-transform: uppercase;
  margin: 0 50px;
}
nav ul li a,
nav ul li a:after,
nav ul li a:before {
  transition: all 0.5s;
}
nav ul li a:active,
nav ul li a:hover {
  color: white;
}

nav .active-link {
  color: white;
  text-decoration: underline;
  text-underline-offset: 5px;
}
</style>
