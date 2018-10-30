<template>
  <v-toolbar color="#313f55" dark>
    <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
    <router-link to="/" style="text-decoration:none">
    <v-toolbar-title style="color:white;text-decoration:none">J Reed Web Design</v-toolbar-title>
    </router-link>
    <v-spacer></v-spacer>
    <div class="hidden-sm-and-down">
      <router-link to="/about">
        <v-btn flat>About</v-btn>
      </router-link>
      <router-link to="/portfolio">
        <v-btn flat>Portfolio</v-btn>
      </router-link>
      <router-link to="/services">
        <v-btn flat>Services</v-btn>
      </router-link>
      <router-link to="/contact">
        <v-btn flat>Contact</v-btn>
      </router-link>
    </div>

    <div class="hidden-md-and-up">
   <v-navigation-drawer v-model="drawer" absolute temporary height="400px">
    <v-toolbar flat >
      <v-list >
        <v-list-tile >
          <v-list-tile-title class="title" >
            Application
          </v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-toolbar>

    <v-divider></v-divider>

    <v-list dense class="pt-0">
      <v-list-tile
        v-for="item in items"
        :key="item.title"

      >
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>

        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
    </div>
  </v-toolbar>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' },
          { title: 'Portfolio', icon: 'business' },
          { title: 'Services', icon: 'build' },
          { title: 'Contact', icon: 'email' }
        ]
      }
    }
  }
</script>
