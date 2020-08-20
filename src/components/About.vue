<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">About</h1>
        </v-row>
        <v-row>
          <v-container id="contactInfo" class="content">
            <v-row>{{ address }}</v-row>
            <v-row>{{ email }}</v-row>
            <v-row>{{ phoneNumber }}</v-row>
          </v-container>
        </v-row>
        <v-row>
          <v-container id="aboutMeBody" class="content">
            <v-row>{{ aboutMeBody }}</v-row>
          </v-container>
        </v-row>
        <v-row>
          <v-container id="socialHandles" class="content">
            <v-row v-for="handle in socialHandles" v-bind:key="handle">
              <a class="navigation-link" href="handle.link">{{ handle.title }}</a>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "About",
  data: () => ({
    address: "Bangalore, India.",
    email: "gauthammk.307@gmail.com",
    phoneNumber: "911-308-1397",
    aboutMeBody:
      "A passionate engineer and a quick learner with a strong understanding of the latest web technologies and application security, equipped with the right technical and soft skills required to propel your organisation in achieving its goals and objectives.",
    socialHandles: [
      {
        title: "GitHub",
        link: "https://github.com/gauthammk",
      },
      {
        title: "LinkedIn",
        link: "https://www.linkedin.com/in/gauthammk/",
      },
      {
        title: "Twitter",
        link: "https://twitter.com/i_amgmk",
      },
    ],
  }),
};
</script>

<style>
.content {
  font-family: "Roboto Mono";
  font-size: 0.9rem;
}
.caption {
  font-family: "Russo One";
}
</style>