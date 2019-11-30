<template>
  <main>
    <welcome />
    <about />
    <webstack />
    <projects />
    <contact />
  </main>
</template>

<script>
import Welcome from "../components/Welcome.vue";
// import About from "./components/About.vue"
// import Webstack from "./components/Webstack.vue"
// import Projects from "./components/Projects.vue"
// import Contact from "./components/Contact.vue"

export default {
  name: "home",
  components: {
    Welcome,
    About: () => import("../components/About.vue"),
    Webstack: () => import("../components/Webstack.vue"),
    Projects: () => import("../components/Projects.vue"),
    Contact: () => import("../components/Contact.vue")
  }
};
</script>
