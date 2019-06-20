<template>
  <div id="app">
    <header>
        <header-buttons />
    </header>
    <main> 
          <welcome />
          <about />
          <webstack />
          <projects />
          <contact />
    </main>
    <footer>
      <a href="https://github.com/simonvea" target="_blank"><img src="./assets/GitHub-Mark-32px.png" alt="GitHub mark"></a>
      <a href="https://www.linkedin.com/in/simon-opheim/" target="_blank"><img src="./assets/In-White-26-┬«.png" alt="LinkedIn logo"></a>
      <br>
      Simon Opheim &copy; 2019
    </footer>
  </div>
</template>

<script>
import HeaderButtons from "./components/Header.vue"
import Welcome from "./components/Welcome.vue"
// import About from "./components/About.vue"
// import Webstack from "./components/Webstack.vue"
// import Projects from "./components/Projects.vue"
// import Contact from "./components/Contact.vue"
import AOS from 'aos'
import 'aos/dist/aos.css'


export default {
  name: 'app',
  components: {
    HeaderButtons,
    Welcome,
    About: () => import("./components/About.vue"),
    Webstack: () => import("./components/Webstack.vue"),
    Projects: () => import("./components/Projects.vue"),
    Contact: () => import("./components/Contact.vue")
  },
  created() {
    AOS.init({
      easing: "ease-in-out",
      throttleDelay: 200
    })
  }
}
</script>

<style>
*,*:after, *:before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-family: 'Ubuntu', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #feffff;
  color: #17252A;
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
  background-color: #2B7a78;
  color: #FEFFFF;
  text-align: center;
  padding-top: 3vh;
}

footer img {
  margin: 0 1vh 2vh;
}

/* ----------------------------------
--------- Transition effects --------
------------------------------------- */

.comp-enter-active, .comp-leave-active {
  transition: opacity .5s;
}
.comp-enter, .comp-leave-to /* .comp-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
