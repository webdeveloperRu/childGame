<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dark
      class="main-navbar"
      height="100px"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2 main-logo"
          contain
          src="./assets/logo.png"
          transition="scale-transition"
        />
        <span style="font-size: 30px">FUNUage</span>
      </div>
      <div >
        <v-btn
            v-for="link in links"
            :key="link"
            text
          >
            {{ link }}
        </v-btn>
      </div>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    links: [
      'Dashboard',
      'Messages',
      'Profile',
      'Updates',
    ]
  }),
};
</script>
<style>
  .main-logo:hover {
    cursor: pointer;
  }
</style>