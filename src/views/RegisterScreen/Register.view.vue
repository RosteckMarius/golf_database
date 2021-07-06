<template>
  <v-container style="width: fit-content">
    <v-col>

      <v-spacer/>

      <v-card class="mb-2">
        <v-card-title class="justify-center">
          Konto erstellen
        </v-card-title>
        <v-divider/>
        <div class="px-8 py-8 pb-0">
          <v-card-text class="ma-0 pa-0">
            Ihr Name
          </v-card-text>
          <v-text-field
              v-model="form.name"
              required
              outlined
              dense>
          </v-text-field>

          <v-card-text class="ma-0 pa-0">
            E-Mail
          </v-card-text>
          <v-text-field
              v-model="form.email"
              :rules="emailPatternRules"
              required
              outlined
              dense>
          </v-text-field>

          <v-card-text class="ma-0 pa-0">
            Passwort
          </v-card-text>
          <v-text-field
              type="password"
              v-model="form.password"
              required
              outlined
              dense>
          </v-text-field>

          <v-card-text class="ma-0 pa-0">
            Passwort erneut eingeben
          </v-card-text>
          <v-text-field
              type="password"
              v-model="form.password2"
              required
              outlined
              dense>
          </v-text-field>

          <v-card-actions>
            <v-spacer/>
            <router-link to="/register" class="justify-center">
              <v-btn
                  dark
                  @click="testGet"
              >
                Sign up
              </v-btn>
            </router-link>
            <v-spacer/>

          </v-card-actions>
        </div>

      </v-card>

      <v-spacer/>
    </v-col>

  </v-container>
</template>

<script lang="ts">
import {RegisterData} from "@/api/api";
import {Component, Vue} from 'vue-property-decorator';
import axios from "axios";

@Component
export default class Register extends Vue {
  form: RegisterData = {
    name: "",
    email: "",
    password: "",
    password2: "",
  };

  token: any
  answer = {}

  emailPatternRules = [
    (content: string) =>
        !content ||
        /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(content) ||
        "Ungültige E-Mail Adresse",
  ];

  sendFeedback() {
    console.log(this.form)
  }

  testLogin() {

    axios.post('https://cloudy.tijazcloud.de/users/login', {
      email: "marius.rosteck@gmail.com",
      password: "test123"
    })
  }

  /*
    testPost() {
      axios.post(
          'https://cloudy.tijazcloud.de/users/register',
          {
            email: this.form.email,
            password: this.form.password
          }
      )

      //axios.post('https://cloudy.tijazcloud.de/users/login')
    }
  */
  testGet() {

    axios.get('https://cloudy.tijazcloud.de/hello', {
      headers: {
        "Authorization": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJtYXJpdXMucm9zdGVja0BnbWFpbC5jb20iLCJpc3MiOiJjbG91ZHkiLCJleHAiOjE2MjU1Njc2MDB9.elIiYOuymAKtHSEdS_0DVyCJfLUP8WnyU8tHWwb2Xvo",
        "Content-Type" : "application/json"
  }
  }).
    then(response => (this.answer = response))
    console.log(this.answer)


  }

}

</script>

<style scoped>

</style>