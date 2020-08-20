<template>
  <v-container fluid class="main-container">
    <v-row class="page pa-10" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Hobbies</h1>
        </v-row>
        <v-row id="hobbies" class="content">{{ hobbies.data }}</v-row>
        <v-row>
          <v-container id="achievements" class="content">
            <v-row
              v-for="achievement in achievements"
              v-bind:key="achievement.id"
            >
              <v-container>
                <v-row class="highlight">{{ achievement.title }}</v-row>
                <v-row>{{ achievement.organisation }}</v-row>
                <v-row class="italicise">{{ achievement.date }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import hobbiesJson from "../content/hobbies.json";
export default {
  name: "Hobbies",
  data: () => ({
    hobbies: hobbiesJson,
  }),
};
</script>

<style></style>
