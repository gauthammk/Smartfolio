<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
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
export default {
  name: "Education",
  data: () => ({
    education: [
      {
        id: 1,
        degree: "B.E in Information Science and Engineering",
        institute: "B.M.S College Of Engineering",
        graduationDate: "2021",
        marks: "9.12 CGPA",
      },
      {
        id: 2,
        degree: "Class 12",
        institute: "DPS Bangalore South(CBSE)",
        graduationDate: "2017",
        marks: "94.6%",
      },
      {
        id: 3,
        degree: "Class 10",
        institute: "DPS Bangalore South(CBSE)",
        graduationDate: "2015",
        marks: "10 CGPA",
      },
    ],
  }),
};
</script>

<style>
.italicise {
  font-style: italic;
  font-weight: 100;
}
</style>