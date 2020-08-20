<template>
  <v-container fluid class="main-container">
    <v-row class="page pa-10" align="center">
      <v-container>
        <v-row align="center" justify="center">
          <h1 class="main-title">
            {{ this.firstName }}
            <span class="highlight">{{ this.lastName }}</span>
          </h1>
        </v-row>
        <v-row align="center" class="content" justify="center">{{
          subtitle
        }}</v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import { first, last, status } from "../content/name.json";

export default {
  name: "Home",
  data: () => ({
    firstName: first,
    lastName: last,
    subtitle: status,
  }),
};
</script>

<style>
.highlight {
  color: #2ecc71;
}
.main-title {
  font-family: "Russo One";
  color: white;
  font-size: 10vw;
}
.page {
  background-color: rgb(34, 34, 34);
  color: white;
  min-height: 100vh;
}
.subtitle {
  font-family: "Russo One";
  color: #2ecc71;
}
.main-container {
  padding-top: 0 !important;
  padding-bottom: 0 !important;
}
</style>
