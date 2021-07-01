<template>
  <v-container style="width: fit-content">
    <v-col>
      <v-card class="mb-2">
        <v-card-title class="justify-center">
          Login to your database
        </v-card-title>
        <v-divider/>
        <div class="px-8 py-8 pb-0">
          <v-card-text class="ma-0 pa-0">
            Username or email adress
          </v-card-text>
          <v-text-field outlined dense></v-text-field>
          <v-card-text class="ma-0 pa-0">
            Password
          </v-card-text>
          <v-text-field outlined dense></v-text-field>
        </div>
        <v-card-actions class="pt-0 pb-8">
          <v-spacer/>
          <v-btn dark>
            Sign in
          </v-btn>
          <v-spacer/>
        </v-card-actions>
      </v-card>

      <v-card outlined>
        <v-card-text class="text-center" onclick="">
          New to Clientbase?
          <a :href="'https://www.google.de'">Sign up here</a>
        </v-card-text>
      </v-card>
    </v-col>
  </v-container>
</template>

<script>
//TODO Sign up link does not forward to Browser
export default {
  name: "Login.component.vue"
}
</script>

<style scoped>

</style>