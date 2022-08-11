<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="12" sm="12" cols="12" lg="10" class="google-font">
          <HeroVue class="my-10" />
          <OverviewVue />
          <!-- <WhatWeDoVue/> -->
          <TechFocusedVue class="my-10" />
          <JoinCommunityVue class="my-10" />
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
// Import your component
// Example
// import xyz from "/path"
import HeroVue from "../components/Home/Hero.vue";
import JoinCommunityVue from '../components/Home/JoinCommunity.vue';
import OverviewVue from "../components/Home/Overview.vue";
import TechFocusedVue from '../components/Home/TechFocused.vue';

// import WhatWeDoVue from '../components/Home/WhatWeDo.vue';



export default {
  name: "HomeComponent",
  components: {
    HeroVue,
    OverviewVue,
    // WhatWeDoVue,
    TechFocusedVue,
    JoinCommunityVue
    // register your component
  },
  data: () => ({}),
  created() {
    document.title = "Home Page | DevFest India";
  },
};
</script>

<style scoped></style>
