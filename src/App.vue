<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-app-bar-nav-icon @click="drawer = !drawer"/>
      <Title :title="title"/>
      <v-spacer/>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
      <Menu/>
    </v-navigation-drawer>
    <v-content>
      <router-view/>
    </v-content>
  <Footer :footer="footer"/>
  </v-app>
</template>

<script>
import Title from '@/views/site/Title'
import Footer from '@/views/site/Footer'
import Menu from '@/views/site/Menu'

export default {
  components: {
    Title,
    Footer,
    Menu
  },
  name: 'App',
  data () {
    return {
      drawer: false,
      title: 'KINGS (한국전력 국제원자력대학원대학교)',
      footer: 'My footer'
    }
  }
}
</script>
