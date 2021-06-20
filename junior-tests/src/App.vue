<template>
  <div id="app">
    <img id="logo" alt="Pretto logo" src="./assets/logo_green.png" @click="toggleIntro" />
    <Intro v-if="displayIntro" @displayFrontTest="toggleFrontTest" @displayIntro="toggleIntro" />
    <FrontTest v-if="displayFrontTest" />
    <img id="wondering-man" alt="Wondering man" src="./assets/wondering-man.png" />
  </div>
</template>

<script>
import Intro from "./components/Intro.vue";
import FrontTest from './components/FrontTest.vue';

export default {
  name: "App",
  data() {
    return {
      displayIntro: true,
      displayFrontTest: false,
    };
  },
  components: {
    Intro,
    FrontTest,
  },
  methods: {
    toggleFrontTest() {
      this.displayIntro = false;
      this.displayFrontTest = true;
    },
    toggleIntro() {
      this.displayIntro = true;
      this.displayFrontTest = false;
    },
  },
};
</script>

<style>
@font-face {
  font-family: "MaisonNeue-Book";
  src: url("./assets/fonts/MaisonNeue-Book.otf") format("opentype");
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: "MaisonNeue-Medium";
  src: url("./assets/fonts/MaisonNeue-Medium.otf") format("opentype");
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: "MaisonNeue-Bold";
  src: url("./assets/fonts/MaisonNeue-Bold.otf") format("opentype");
  font-weight: 700;
  font-style: normal;
}

@font-face {
  font-family: "MaisonNeue-Black";
  src: url("./assets/fonts/MaisonNeue-Black.otf") format("opentype");
  font-weight: 900;
  font-style: normal;
}
button {
  font-family: "MaisonNeue-Medium";
  font-size: 16px;
  background-color: #fc5c63;
  color: rgb(250, 250, 250);
  padding: 15px 20px;
  border: none;
}
button:hover {
  background-color: #fc847c;
  cursor: pointer;
}
h1 {
  font-family: "MaisonNeue-Black";
}
h2,
h3,
h4,
h5,
h6 {
  font-family: "MaisonNeue-Bold";
}
a {
  color: #006855;
}
#app {
  font-family: MaisonNeue-Book;
  text-align: center;
  color: rgb(30, 30, 30);
  margin-top: 60px;
}
#logo {
  max-width: 24vw;
}
#logo:hover {
  cursor: pointer;
}
#wondering-man {
  position: fixed;
  max-width: 10vw;
  bottom: 30px;
  right: 30px;
}
.large {
  width: 100%;
  max-width: 500px;
}
</style>
