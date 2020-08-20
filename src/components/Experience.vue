<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
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
export default {
  name: "Experience",
  data: () => ({
    experience: [
      {
        id: 1,
        role: "Cyber Security Intern",
        organisation: "DailyObjects.com",
        timeline: "13th July 2020 - Present",
        description:
          "Performing website penetration testing and REST API security vulnerability analysis according to the OWASP guidelines using BurpSuite and Postman.",
      },
      {
        id: 2,
        role: "Research and Development Intern",
        organisation: "Samsung R&D Institue Bangalore",
        timeline: "3rd February 2020 - 1st June 2020",
        description:
          "Created an Android app to analyse call record and SMS data from an android phone to predict a new contact's identifying group.",
      },
      {
        id: 3,
        role: "Information Security Intern",
        organisation: "Sumeru Software Solutions Pvt. Ltd.",
        timeline: "June 1st 2019 - June 30th 2019",
        description:
          "PentesterLab Bootcamp in a simulated project environment to understand application and network security in detail and used the gained experience for attending and organising multiple CTF events with a participation of over 100 students across colleges.",
      },
      {
        id: 4,
        role: "Vice President",
        organisation: "Hackers' Club of BMSCE",
        timeline: "August 2019 - present",
        description:
          "Designed and organised AnonCTF-2019, an annual intra college cyber security hackathon. Conducted a Lec-Dem on SQL Injection. Helped fellow cyber security enthusiasts gain a platform to showcase their work.",
      },
    ],
  }),
};
</script>

<style>
</style>