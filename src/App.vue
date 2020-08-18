<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <Navbar />
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Title />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <About />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Education />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Experience />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Skills />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Projects />
          </v-col>
        </v-row>
      </v-container>
      <v-divider></v-divider>
      <v-container fluid>
        <v-row>
          <v-col>
            <Hobbies />
          </v-col>
        </v-row>
      </v-container>
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
.container {
  background-color: rgb(34, 34, 34);
  color: white;
}
</style>