<template>
  <v-footer
    height="auto"
    color="primary lighten-1"
  >
    <v-layout
      justify-center
      row
      wrap
    >
      <v-flex
        primary
        lighten-2
        py-3
        text-xs-center
        white--text
        xs12
      >
        <p>All servers are managed here</p>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us'
      ]
    })
  }
</script>