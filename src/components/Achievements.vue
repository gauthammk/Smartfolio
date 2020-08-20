<template>
  <v-container fluid class="main-container">
    <v-row class="page" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Achievements</h1>
        </v-row>
        <v-row>
          <v-container class="content">
            <v-row>
              <v-col>
                <v-row
                  v-for="achievement in curricularAchievements"
                  v-bind:key="achievement.id"
                >
                  <v-container>
                    <v-row class="highlight">{{ achievement.title }}</v-row>
                    <v-row class="italicise">{{ achievement.date }}</v-row>
                    <v-row>{{ achievement.organisation }}</v-row>
                  </v-container>
                </v-row>
              </v-col>
              <v-col>
                <v-row
                  v-for="achievement in coCurricularAchievements"
                  v-bind:key="achievement.id"
                >
                  <v-container>
                    <v-row class="highlight">{{ achievement.title }}</v-row>
                    <v-row class="italicise">{{ achievement.date }}</v-row>
                    <v-row>{{ achievement.organisation }}</v-row>
                  </v-container>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import {
  curricularAchievements,
  coCurricularAchievements,
} from "../content/achievements.json";
export default {
  name: "Achivements",
  data: () => ({
    curricularAchievements: curricularAchievements,
    coCurricularAchievements: coCurricularAchievements,
  }),
};
</script>

<style></style>
