<template>
  <v-container fluid class="main-container">
    <v-row class="page" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Education</h1>
        </v-row>
        <v-row>
          <v-container id="education" class="content">
            <v-row v-for="ed in education" v-bind:key="ed.id">
              <v-container>
                <v-row class="highlight">{{ ed.institute }}</v-row>
                <v-row>{{ ed.degree }}</v-row>
                <v-row class="italicise">Year of graduating: {{ ed.graduationDate }}</v-row>
                <v-row>{{ ed.marks }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import educationJson from "../content/education.json";

export default {
  name: "Education",
  data: () => ({
    education: educationJson,
  }),
};
</script>

<style>
.italicise {
  font-style: italic;
  font-weight: 100;
}
</style>