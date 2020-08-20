<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">Hobbies</h1>
        </v-row>
        <v-row id="hobbies" class="content">{{ hobbies }}</v-row>
        <v-row>
          <v-container id="achievements" class="content">
            <v-row v-for="achievement in achievements" v-bind:key="achievement.id">
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
export default {
  name: "Hobbies",
  data: () => ({
    hobbies:
      "Apart from work, I am a Carnatic vocalist and violinist. I have performed across Bangalore and I continue to practice my art in my free time. I also enjoy spending time outdoors and am a travel photographer. Discovering new cultures, food and traditions is something I am deeply passionate about. When forced indoors, I resort to reading action thriller novels. A few of my favourites include Mario Puzo's 'The Godfather' and Lee Child's 'Persuader'. I am a novice chef and find joy in cooking for family and friends. Being a tech and gadget fanatic, I try to keep myself constantly updated on the latest news and trends in the field.",
    achievements: [
      {
        id: 1,
        title: "Lensation Photography Competition | 1st Place ",
        date: "September 2017",
        organisation: "BMSCE Phaseshift",
      },
      {
        id: 2,
        title: "Karnataka Music Senior Grade | Vocal ",
        date: "May 2018",
        organisation: "Karnataka State Education Board",
      },
      {
        id: 3,
        title: "Karnataka Music Junior Grade | Violin ",
        date: "October 2015",
        organisation: "Karnataka State Education Board",
      },
    ],
  }),
};
</script>

<style>
</style>