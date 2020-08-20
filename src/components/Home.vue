<template>
  <v-container fluid class="main-container">
    <v-row class="main-title" align="center">
      <v-container>
        <v-row align="center" justify="center">
          <h1 class="main-heading">
            Gautham
            <span class="highlight">MK</span>
          </h1>
        </v-row>
        <v-row align="center" class="content" justify="center">Forever Curious.</v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style>
.highlight {
  color: #2ecc71;
}
.main-heading {
  font-size: 7rem;
  font-family: "Russo One";
  color: white;
}
.main-title {
  background-color: rgb(34, 34, 34);
  color: white;
  height: 100vh;
}
.subtitle {
  font-family: "Russo One";
  color: #2ecc71;
}
.main-container {
  padding: 0 !important;
}
</style>