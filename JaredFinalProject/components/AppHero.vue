<template>
<div>
  <v-jumbotron
    :gradient="gradient"
    dark
    src="https://jreedwebdesign.com/wp-content/uploads/2018/04/hero-home-page-1024x682.jpg"
  >
    <v-container fill-height>
      <v-layout align-center>
        <v-flex text-xs-center>
          <h1 class="display-3">Welcome</h1>
          <h4 class="subheading lg">Web Design, SEO and Website Hosting</h4>
        </v-flex>
      </v-layout>
    </v-container>
  </v-jumbotron>
</div>
</template>

<script>
  export default {
    data: () => ({
      gradient: 'to top right, rgba(49,81,181, .3), rgba(25,32,72, .7)'
    })
  }
</script>