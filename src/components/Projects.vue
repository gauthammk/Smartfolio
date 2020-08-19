<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="left">
          <h1 class="subtitle">Projects</h1>
        </v-row>
        <v-row>
          <v-container id="projects" class="content">
            <v-row v-for="project in projects" v-bind:key="project.id">
              <v-container>
                <v-row class="highlight">{{ project.title }}</v-row>
                <v-row>{{ project.description }}</v-row>
                <v-row justify="start">
                  <v-col md="auto" style="padding: 0;" v-if="project.demo">
                    <a class="hyperlink" href="project.demo">Demo</a>|
                  </v-col>
                  <v-col md="auto" style="padding: 0;" v-if="project.github">
                    <a class="hyperlink" href="project.github">GitHub</a>
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
  name: "Projects",
  data: () => ({
    projects: [
      {
        id: 1,
        title: "Network Pentesting With RaspberryPi4",
        description:
          "Targeted packet sniffing, Wifi cracking, MITM attacks, Server side attacks using Metasploit and client side attacks using BeEf.",
        demo: null,
        github: null,
      },
      {
        id: 2,
        title: "Ideate",
        description:
          "A simple web app where users can look for inspirational ideas among different categories and also put forth their unique content. Built with Python + Django and PostgreSQL. Deployed with Heroku.",
        demo: "http://ideateapp.herokuapp.com/",
        github: "https://github.com/gauthammk/Ideate",
      },
      {
        id: 3,
        title: "Pathfinder",
        description:
          "Interactive visualisations of popular pathfinding algorithms like Dijkstra's algorithm, DFS and BFS in the browser. Built with Vue.js and Vuetify. Deployed with Netlify.",
        demo: "http://gauthammk-pathfinder.netlify.app/",
        github: "https://github.com/gauthammk/Pathfinder",
      },
      {
        id: 4,
        title: "PyQuiz",
        description:
          "A minimal yet robust API for quiz applications built with Django and the Django REST Framework.",
        demo: null,
        github: "https://github.com/gauthammk/PyQuiz",
      },
      {
        id: 5,
        title: "The Lazy Chef",
        description:
          "A web app to find interesting recipes based on the items in your kitchen. Built with Vue.js and Vuetify.",
        demo: "https://gauthammk.github.io/the-lazy-chef/",
        github: "https://github.com/gauthammk/the-lazy-chef",
      },
      {
        id: 6,
        title: "Restaurant Recommendation Engine",
        description:
          "A content based recommendation engine that uses cosine correlation and sources data using the Zomato API.",
        demo: null,
        github: "https://github.com/gauthammk/restaurant-recommendation-engine",
      },
    ],
  }),
};
</script>

<style>
.hyperlink {
  color: #2ecc71 !important;
}
</style>