<template>
  <v-container fluid class="main-container">
    <v-app-bar fixed hide-on-scroll class="navbar">
      <v-row align="center">
        <v-col>
          <v-btn x-large icon class="navigation-button" v-on:click="greet">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </v-col>
        <!-- <v-btn @click="$vuetify.goTo('#about')">Scroll Test</v-btn> -->
        <v-col md="auto">
          <v-toolbar-title class="main-heading">
            <span>&lt; G</span>
            <span class="highlight">MK</span>
            <span>/ &gt;</span>
          </v-toolbar-title>
        </v-col>
      </v-row>
    </v-app-bar>
  </v-container>
</template>

<script>
export default {
  name: "Navbar",
  methods: {
    greet: function () {
      alert("Hello world!");
    },
  },
};
</script>

<style scoped>
.navbar {
  background-color: rgb(34, 34, 34) !important;
}
.navigation-button {
  color: #2ecc71 !important;
}
</style>