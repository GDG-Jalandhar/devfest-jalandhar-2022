<template>
  <v-container fluid class="my-10">
    <v-row>
      <v-col class="text-center google-font">
        <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">Our Sponsors</p>
        <p>
          Sponsors dedicated to building remarkable experience!
        </p>
        <v-btn depressed rounded color="#4285F4" dark href="https://bit.ly/dfj-22-sponsorship-form" target="_blank" class="mx-1 mt-1"
          >Become a Sponsor</v-btn
        >
        <v-btn depressed rounded color="#4285F4" target="_blank" href="https://bit.ly/dfj-22-sponsorship-brochure" outlined class="mx-1 mt-1"
          >Sponsorship Brochure</v-btn
        >
      </v-col>
    </v-row>
    <v-row class="mx-md-16 px-md-12" justify="center" align="center">
      <v-col md="12" class="text-center">
        <!-- {{item.image}} -->
        <span
          v-for="(item, index) in pastEvents"
          :key="index"
          style="padding: 10px"
        >
          <a :href="item.link" target="_blank">
            <img :src="item.image" :width="item.size" alt="" />
          </a>
        </span>

        
<!-- 
        <p class="google-font mt-10">Platinum Sponsors</p>
        <a href="https://www.connectzone.in/" target="_blank" class="mx-2">
          <img
            src="https://www.connectzone.in/assets/connect-broadband-logo-white.png"
            width="150px"
            alt=""
          />
        </a>
        <a href="https://digimantralabs.com/" target="_blank" class="mx-2">
          <img
            :src="require('@/assets/img/sponsors/digimantra.jpg')"
            width="220px"
            alt=""
          />
        </a>

        <p class="google-font mt-10">Silver Sponsors</p>
        <a href="https://www.allsoftsolutions.in/IBM/Main" target="_blank">
          <img
            src="https://www.allsoftsolutions.in/IBM/assets/logo/Logo-Small.png"
            width="240px"
            alt=""
          />
        </a>


        <p class="google-font mt-10">Venue Partner</p>
        <a href="https://www.pyramidcollege.edu.in/" target="_blank">
          <img
            src="https://www.pyramidcollege.edu.in/images/pcbt-logo-2022.png"
            width="150px"
            alt=""
          />
        </a> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "SponsorComponent",
  data: () => ({
    pastEvents: [
      {
        title: "Google Developers",
        size: "250px",
        image:
          "https://www.gstatic.com/devrel-devsite/prod/vdb149cdc08c87ab249cdebfec6395e8f073056d752ca9c2d285d3b8426fcfa32/developers/images/lockup.svg",
        link: "https://developers.google.com/",
      }
    ],
  }),
};
</script>

<style>
</style>