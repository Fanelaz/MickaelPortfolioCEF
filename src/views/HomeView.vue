<template>
  <body>
    <div class="desc">
      <div id="name" class="name">
        <h1>
          <span>M</span>
          <span>I</span>
          <span>C</span>
          <span>K</span>
          <span>A</span>
          <span>E</span>
          <span>L</span>
        </h1>
      </div>
      <p id="presentation">
        Je suis un jeune développeur en pleine formation depuis le 05 septembre
        2023. <br />
        Je suis très motivé dans les projets qui touchent le monde de la
        programmation, depuis l'âge de mes 10 ans je souhaite en faire mon
        métier !!
      </p>

      <img
        class="img-logo"
        src="../assets/imgs/icons8-html-48.png"
        alt="logo HTML"
      />
      <img
        class="img-logo"
        src="../assets/imgs/icons8-css-48.png"
        alt="logo CSS"
      />
      <img
        class="img-logo"
        src="../assets/imgs/icons8-javascript-48.png"
        alt="logo JAVASCRIPT"
      />
    </div>

    
  </body>
</template>

<script></script>

<style scoped>

@import url("https://fonts.googleapis.com/css2?family=Cabin&family=Roboto+Condensed:wght@100&family=Roboto:ital,wght@0,100;1,100&display=swap");


body {
  width: auto;
  height: auto;
  text-align: center;
  display: flex;
  justify-content: center;
}


.desc {
  width: 100%;
  align-content: center;
  padding-bottom: 200px;
  font-family: Cabin;
}

.name {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  color: #8AAEE0;
margin: 100px 0 100px 0 ;
}

h1 {
  margin: 0%;
  padding: 0%;
  font-size: 3em; /* Ajustez la taille du texte selon vos besoins */
  color: #8AAEE0; /* Couleur du texte */
  font-family: "Roboto Mono", monospace;
}

h1 span {
  margin: 20px;
  display: table-cell;
  padding: 10px;
  animation: animate 3s ease infinite;
}

h1 span:nth-child(1) {
  animation-delay: 0s;
}
h1 span:nth-child(2) {
  animation-delay: 0.3s;
}
h1 span:nth-child(3) {
  animation-delay: 0.6s;
}
h1 span:nth-child(4) {
  animation-delay: 0.9s;
}
h1 span:nth-child(5) {
  animation-delay: 1.2s;
}
h1 span:nth-child(6) {
  animation-delay: 1.6s;
}
h1 span:nth-child(7) {
  animation-delay: 1.9s;
}

.img-logo {
  width: 100px;
  padding-left: 30px;
}

#presentation {
  font-size: 24px;
  color: black;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}

#presentation:hover {
  text-shadow: #B1C9EF 1px 0 10px;
}

@keyframes animate {
  0%,
  100% {
    color: #fff;
    filter: blur(2px);
    text-shadow: 0 0 10px #fff;
  }

  5%,
  95% {
    color: #8AAEE0;
    filter: blur(0px);
    text-shadow: none;
  }
}
</style>
