<template>
  <v-card
      height="400"
      width="256"
      class="mx-auto"
  >
    <v-navigation-drawer permanent>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            CLIENTBASE
          </v-list-item-title>
          <v-list-item-subtitle>
            Marius Rosteck
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
          dense
          nav
      >
        <v-list-item
            v-for="item in items"
            :key="item.title"
            link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
  name: "MainMenu.view",
  data(){
    return{
      items:[
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Students', icon: 'mdi-image' },
        { title: 'About', icon: 'mdi-help-box' },
      ]
    }
  }
}
</script>

<style scoped>

</style>