<template>
  <v-container fluid class="main-container">
    <v-row class="page pa-10" align="center">
      <v-container>
        <v-row align="center" justify="start">
          <h1 class="subtitle">About</h1>
        </v-row>
        <v-row>
          <v-container id="contactInfo" class="content">
            <v-row v-for="contact in contacts" v-bind:key="contact.id">
              <v-container>
                <v-row class="highlight">{{ contact.title }}</v-row>
                <v-row>{{ contact.data }}</v-row>
              </v-container>
            </v-row>
          </v-container>
        </v-row>
        <v-row>
          <v-container id="aboutMeBody" class="content">
            <v-row>{{ about.data }}</v-row>
          </v-container>
        </v-row>
        <v-row>
          <v-container id="socialHandles" class="content">
            <v-row v-for="handle in socialHandles" v-bind:key="handle.id">
              <a class="navigation-link" :href="handle.link">{{
                handle.title
              }}</a>
            </v-row>
          </v-container>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<script>
import socialHandlesJson from "../content/socialHandles.json";
import aboutJson from "../content/about.json";
import contactsJson from "../content/contacts.json";
export default {
  name: "About",
  data: () => ({
    contacts: contactsJson,
    about: aboutJson,
    socialHandles: socialHandlesJson,
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
