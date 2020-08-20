<template>
  <v-container fluid class="main-container">
    <v-row class="page" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Certifications</h1>
        </v-row>
        <v-row>
          <v-container class="content">
            <v-row v-for="certification in certifications" v-bind:key="certification.id">
              <v-container>
                <v-row class="highlight">{{ certification.title }}</v-row>
                <v-row class="italicise">{{ certification.date }}</v-row>
                <v-row>{{ certification.organisation }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import certificationsJson from "../content/certifications.json";
export default {
  name: "Certifications",
  data: () => ({
    certifications: certificationsJson,
  }),
};
</script>

<style>
</style>