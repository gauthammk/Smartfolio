<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center" justify="center">
      <v-container>
        <v-row align="center" justify="center">
          <h1 class="main-heading">
            Gautham
            <span class="highlight">MK</span>
          </h1>
        </v-row>
        <v-row align="center" justify="center">Subtitle</v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Title",
};
</script>

<style>
.highlight {
  color: rgb(197, 0, 0);
}
.main-heading {
  font-size: 7rem;
  font-family: "Russo One";
}
.main-title {
  background-color: rgb(34, 34, 34);
  color: white;
  height: 100vh;
}
.subtitle {
  margin-top: 2rem;
  font-family: "Russo One";
}
.main-container {
  padding: 0 !important;
}
</style>