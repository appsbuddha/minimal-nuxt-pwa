<template>
  <v-app light>
    <v-app-bar app light>
      <v-spacer />
      <v-app-bar-nav-icon @click.native.stop="drawer = !drawer"/>
    </v-app-bar>
    <v-content>
      <v-navigation-drawer right app class="pa-3" v-model="drawer">
        <v-list class="d-flex flex-column">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <nuxt-link to="/" class="nav-link">Home</nuxt-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <nuxt-link to="/second" class="nav-link">Second</nuxt-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      title: 'MVP',
      drawer: false
    }
  },

}
</script>