<template>
  <v-app>
    <v-app-bar
      app
      dark
    >
      <div class="d-flex align-center">
        <v-img
          class="shrink mr-2"
          contain
          :src="require('./assets/testlogo.png')"
          transition="scale-transition"
          width="40"
        />

        <v-img
          contain
          min-width="100"
          :src="require('./assets/Name.png')"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HomeScreen/>
    </v-main>
  </v-app>
</template>

<script>
import HomeScreen from './components/HomeScreen';

export default {
  name: 'App',

  components: {
    HomeScreen,
  },

  data: () => ({
    //
  }),
};
</script>
