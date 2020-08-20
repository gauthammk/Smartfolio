<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="start">
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
import skillsJson from "../content/skills.json";
export default {
  name: "Skills",
  data: () => ({
    skills: skillsJson,
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