<template>
  <v-app>
    <v-main>
      <Navbar @menu-clicked-event="handleMenuClick" />
      <v-divider class="divider"></v-divider>
      <Home id="home" />
      <v-divider class="divider"></v-divider>
      <About id="about" />
      <v-divider class="divider"></v-divider>
      <Education id="education" />
      <v-divider class="divider"></v-divider>
      <Experience id="experience" />
      <v-divider class="divider"></v-divider>
      <Skills id="skills" />
      <v-divider class="divider"></v-divider>
      <Projects id="projects" />
      <v-divider class="divider"></v-divider>
      <Hobbies id="hobbies" />
      <v-divider class="divider"></v-divider>
    </v-main>
  </v-app>
</template>

<script>
import Home from "./components/Home";
import Navbar from "./components/Navbar";
import About from "./components/About";
import Education from "./components/Education";
import Experience from "./components/Experience";
import Skills from "./components/Skills";
import Projects from "./components/Projects";
import Hobbies from "./components/Hobbies";

export default {
  name: "App",

  components: {
    Home,
    Navbar,
    About,
    Education,
    Experience,
    Skills,
    Projects,
    Hobbies,
  },

  data: () => ({
    isMenuClicked: false,
    overlay: false,
    absolute: true,
  }),
  methods: {
    handleMenuClick: function () {
      console.log("Menu clicked.");
      this.isMenuClicked = !this.isMenuClicked;
    },
  },
};
</script>
<style>
.divider {
  background-color: #2ecc71;
}
</style>