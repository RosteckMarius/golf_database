<template>
  <v-app>
    <v-app-bar
        app
        dark
    >
      <div class="d-flex align-center">
        <DropdownMenu></DropdownMenu>
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
      <router-view>
        <LoginScreen></LoginScreen>
      </router-view>
    </v-main>

  </v-app>
</template>

<script>
import LoginScreen from './views/LoginScreen/Login.view';
import DropdownMenu from './components/DropdownMenu.component.vue'
//import StudentsScreen from './views/StudentsScreen/StudentsScreen.view';
//import MainMenu from './views/MainMenu/MainMenu.view'

export default {
  name: 'App',

  components: {
    LoginScreen,
    DropdownMenu,


  },

  data: () => ({
    //
  }),
};
</script>
