<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <Navbar />
      </v-container>
      <v-divider class="divider"></v-divider>
      <Title />
      <v-divider class="divider"></v-divider>
      <About />
      <v-divider class="divider"></v-divider>
      <Education />
      <v-divider class="divider"></v-divider>
      <Experience />
      <v-divider class="divider"></v-divider>
      <Skills />
      <v-divider class="divider"></v-divider>
      <Projects />
      <v-divider class="divider"></v-divider>
      <Hobbies />
      <v-divider class="divider"></v-divider>
    </v-main>
  </v-app>
</template>

<script>
import Title from "./components/Title";
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
    Title,
    Navbar,
    About,
    Education,
    Experience,
    Skills,
    Projects,
    Hobbies,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
.divider {
  background-color: #2ecc71;
}
</style>