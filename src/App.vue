<template>
  <div id="app">
    <header>
      <header-buttons />
    </header>
    <router-view></router-view>
    <footer>
      <a href="https://github.com/simonvea" target="_blank">
        <img src="./assets/GitHub-Mark-32px.png" alt="GitHub mark" />
      </a>
      <a href="https://www.linkedin.com/in/simon-opheim/" target="_blank">
        <img src="./assets/In-White-26-┬«.png" alt="LinkedIn logo" />
      </a>
      <br />Simon Opheim &copy; 2019
    </footer>
  </div>
</template>

<script>
import HeaderButtons from "./components/Header";
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "app",
  components: { HeaderButtons },
  created() {
    AOS.init({
      easing: "ease-in-out",
      throttleDelay: 200
      //once: true,
    });
  }
};
</script>

<style>
*,
*:after,
*:before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-family: "Ubuntu", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #feffff;
  color: #17252a;
}

header {
  top: 0;
  position: fixed;
  background: transparent;
  display: flex;
  justify-content: flex-end;
  width: 100%;
}

footer {
  bottom: 0;
  height: 15vh;
  width: 100%;
  background-color: #2b7a78;
  color: #feffff;
  text-align: center;
  padding-top: 3vh;
}

footer img {
  margin: 0 1vh 2vh;
}

/* ----------------------------------
--------- Transition effects --------
------------------------------------- */

.comp-enter-active,
.comp-leave-active {
  transition: opacity 0.5s;
}
.comp-enter, .comp-leave-to /* .comp-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
