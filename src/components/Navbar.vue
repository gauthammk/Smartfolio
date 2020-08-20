<template>
  <v-container fluid class="main-container">
    <v-app-bar fixed hide-on-scroll class="navbar">
      <v-row align="center">
        <v-col>
          <v-btn x-large icon class="navigation-button" v-on:click="overlay = !overlay">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </v-col>
        <v-col md="auto">
          <v-toolbar-title class="main-title">
            <span>&lt; {{firstName.substring(0,1)}}</span>
            <span class="highlight">{{lastName.substring(0,2)}}</span>
            <span>/ &gt;</span>
          </v-toolbar-title>
        </v-col>
      </v-row>
    </v-app-bar>
    <v-scroll-x-transition>
      <v-overlay :value="overlay" opacity="0.95">
        <v-row style="height: 100vh; width: 100vw;" align="center">
          <v-container>
            <v-row>
              <v-btn icon @click="overlay = false" class="navigation-button">
                <v-icon>mdi-close</v-icon>
              </v-btn>
            </v-row>
            <v-row align="center">
              <h1 class="subtitle">Menu</h1>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#home')">Home</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#about')">About</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#education')">Education</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#experience')">Experience</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#skills')">Skills</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#projects')">Projects</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#achievements')">Achivements</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#certifications')">Certifications</a>
            </v-row>
            <v-row class="content">
              <a class="navigation-link" @click="scrollToId('#hobbies')">Hobbies</a>
            </v-row>
          </v-container>
        </v-row>
      </v-overlay>
    </v-scroll-x-transition>
  </v-container>
</template>

<script>
import { first, last } from "../content/name.json";

export default {
  name: "Navbar",
  data: () => ({
    overlay: false,
    firstName: first,
    lastName: last,
  }),
  methods: {
    triggerMenu: function () {
      this.$emit("menu-clicked-event");
    },
    scrollToId: function (id) {
      this.$vuetify.goTo(id);
      this.overlay = false;
    },
  },
};
</script>

<style>
.navbar {
  background-color: rgb(34, 34, 34) !important;
}
.navigation-button {
  color: #2ecc71 !important;
}
.navigation-link {
  color: white !important;
}
.navigation-link:hover {
  color: #2ecc71 !important;
}
</style>