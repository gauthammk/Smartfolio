<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Achievements</h1>
        </v-row>
        <v-row>
          <v-container class="content">
            <v-row v-for="achievement in achievements" v-bind:key="achievement.id">
              <v-container>
                <v-row class="highlight">{{ achievement.title }}</v-row>
                <v-row class="italicise">{{ achievement.date }}</v-row>
                <v-row>{{ achievement.organisation }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import achivementsJson from "../content/achievements.json";
export default {
  name: "Achivements",
  data: () => ({
    achievements: achivementsJson,
  }),
};
</script>

<style>
</style>