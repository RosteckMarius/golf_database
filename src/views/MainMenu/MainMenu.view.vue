<template>
  <v-card
      height="100%"
      width="256"
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
            :to="item.route"
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
  data() {
    return {
      items: [
        {title: 'Dashboard', icon: 'mdi-view-dashboard', route: '/'},
        {title: 'Students', icon: 'mdi-image', route: '/students'},
        {title: 'About', icon: 'mdi-help-box', route: '/login'},
      ]
    }
  }
}
</script>

<style scoped>

</style>