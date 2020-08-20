<template>
  <v-container fluid class="main-container">
    <v-row class="page" align="center">
      <v-container>
        <v-row align="center" justify="start">
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
                    <a class="navigation-link" :href="project.demo">Demo</a>|
                  </v-col>
                  <v-col md="auto" style="padding: 0;" v-if="project.repo">
                    <a class="navigation-link" :href="project.repo">Repo</a>
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
import projectsJson from "../content/projects.json";

export default {
  name: "Projects",
  data: () => ({
    projects: projectsJson,
  }),
};
</script>

<style></style>
