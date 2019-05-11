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
    </main>
    <footer>
      Copyright Simon Opheim &copy; 2019
    </footer>
  </div>
</template>

<script>
import HeaderButtons from "./components/Header.vue"
import Welcome from "./components/Welcome.vue"
import About from "./components/About.vue"
import Webstack from "./components/Webstack.vue"
import Projects from "./components/Projects.vue"


export default {
  name: 'app',
  components: {
    HeaderButtons,
    Welcome,
    About,
    Webstack,
    Projects
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
  padding-top: 7vh;
}
</style>
