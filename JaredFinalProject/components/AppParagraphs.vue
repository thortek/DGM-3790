<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap class="card">
      <v-flex v-for="i in 1" :key="`6${i}`" xs6>
        
          <v-card-text class="px-0">
              <h3>About Us</h3>
              <p>We are a Utah based web design, SEO and website hosting company that strives to create websites that are more “user friendly” than other websites out there. Too often we find that many people struggle to find the necessary information they are looking for on a website. Our mission is to give your business that leading edge that your competition does not have. We are driven to make you successful online.</p>
          </v-card-text>
        
      </v-flex>
      <v-flex v-for="i in 1" :key="`6${i}`" xs6>
        
          <v-card-text class="px-0">
              <h3>User Friendly All The Way</h3>
              <p>Let your users find the information they need with ease. Don’t allow them to be frustrated and leave your website. Consider your customers first and consider how you would feel looking for information that’s hiding.</p>
          </v-card-text>
        
      </v-flex>
     </v-layout>
  </v-container>
</template>

<style>

.card {
    padding-top: 50px;
    padding-bottom: 50px;
}
h3 {
    padding-bottom: 15px;
    padding-left: 30px;
}
p {
    padding-left: 30px;
    padding-right: 30px;
}
</style>