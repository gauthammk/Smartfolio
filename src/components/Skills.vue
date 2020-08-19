<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="left">
          <h1 class="subtitle">Skills</h1>
        </v-row>
        <v-row>
          <v-container id="skills" class="content">
            <v-row v-for="skill in skills" v-bind:key="skill.id" align="center">
              <v-container>
                <v-row align="center">
                  <v-col style="padding: 0;" cols="4">{{ skill.title }}</v-col>
                  <v-col style="padding: 0;" cols="2">
                    <v-progress-linear color="#2ecc71" height="5" :value="skill.score"></v-progress-linear>
                  </v-col>
                </v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Skills",
  data: () => ({
    skills: [
      {
        id: 1,
        title: "Information Security and Ethical Hacking",
        score: 75,
      },
      {
        id: 2,
        title: "Linux and Git",
        score: 75,
      },
      {
        id: 3,
        title: "Python and Django",
        score: 75,
      },
      {
        id: 4,
        title: "Node.js, Express.js & Vue.js",
        score: 60,
      },
      {
        id: 5,
        title: "HTML5, CSS3 & Bootstrap",
        score: 75,
      },
      {
        id: 6,
        title: "MySQL & Django ORM",
        score: 60,
      },
      {
        id: 7,
        title: "Java and OOP",
        score: 60,
      },
      {
        id: 8,
        title: "Android app development",
        score: 35,
      },
    ],
  }),
};
</script>

<style>
.right-justify {
  justify-content: end !important;
  justify-items: end !important;
  justify-self: end !important;
}
</style>