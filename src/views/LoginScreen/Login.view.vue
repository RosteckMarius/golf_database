<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12 pb-0">
        <v-img
            :src="require('../../assets/logo.png')"
            class="my-3"
            contain
            height="200"
        />
        <v-col class="mb-4">
          <h2 class="font-weight-regular">
            WELCOME TO CLIENTBASE
          </h2>
        </v-col>
      </v-col>
    </v-row>
    <v-row>
    <v-spacer/>
    <login dark></login>
    <v-spacer/>
    </v-row>
  </v-container>
</template>

<script>
import login from "@/components/LoginScreen.component"

export default {
  name: 'Login',
  components: {
    login
  },

}
</script>
