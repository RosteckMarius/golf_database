<template>
  <v-container>
    <h2 class="font-weight-regular text-center pa-10">
      STUDENTS OVERVIEW
    </h2>
    <v-data-table
        :headers="headers"
        :items="students"
        :items-per-page="5"
        class="elevation-1"
    ></v-data-table>
  </v-container>
</template>

<script>
export default {
  name: "StudentsScreen.view",
  data() {
    return {
      headers: [

        {text: "Vorname", align: "start", value: "vorname",},
        {text: "Nachname", align: "start", value: "nachname",},
        {text: "Email", align: "start", value: "email",},
        {text: "Telefon", align: "start", value: "telefon",},

      ],
      students: [
        {vorname: "Marius", nachname: "Rosteck", email: "marius.rosteck@gmail.com", telefon: "01631624948"},
        {vorname: "Theresa", nachname: "Kunzfeld", email: "t.kunzfeld@gmail.com", telefon: "0112321323"}
      ]
    }
  }
}
</script>

<style scoped>

</style>