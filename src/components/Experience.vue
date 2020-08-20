<template>
  <v-container fluid class="main-container">
    <v-row class="page" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Experience</h1>
        </v-row>
        <v-row>
          <v-container id="experience" class="content">
            <v-row v-for="exp in experience" v-bind:key="exp.id">
              <v-container>
                <v-row class="highlight">{{ exp.role }}</v-row>
                <v-row>{{ exp.organisation }}</v-row>
                <v-row class="italicise">{{ exp.timeline }}</v-row>
                <v-row>{{ exp.description }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import experienceJson from "../content/experience.json";

export default {
  name: "Experience",
  data: () => ({
    experience: experienceJson,
  }),
};
</script>

<style>
</style>