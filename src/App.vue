<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <Navbar />
      </v-container>
      <v-divider></v-divider>
      <Title />
      <v-divider></v-divider>
      <About />
      <v-divider></v-divider>
      <Education />
      <v-divider></v-divider>
      <Experience />
      <v-divider></v-divider>
      <Skills />
      <v-divider></v-divider>
      <Projects />
      <v-divider></v-divider>
      <Hobbies />
      <v-divider></v-divider>
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
<style scoped>
</style>