<template>
  <v-container fluid>
    <v-row justify="center" align="center">
      <v-col md="12" class="">
        <v-container fluid>
          <v-row justify="center" align="center">
            <!-- grey lighten-4 -->
            <v-col md="7" class="px-0 pr-md-10" style="border-radius: 16px">
              <!-- <div class="px-7 my-8" style=""> -->
                <!-- <p class="gdg-heading">DevFest Jalandhar</p> -->
                <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">What's New in DevFest</p>

                <p
                  class="google-font text--secondary"
                  style="font-weight: 500; font-size: 18px"
                >
                This DevFest will be an achievement for the GDG Jalandhar Team as we are all set to host the 2000+ developers by connecting the dots which we have started since a month. We started with the theme of Building Developers at DevCommunity Roadshow, then Guiding Developers at DevCreate Hackathon and now, ready with the theme - Supporting Developers.
                </p>

                <v-container fluid class="pa-0 ma-0" style="border-radius: 12px" >
                  <v-row align="start" justify="start">
                    <v-col
                      cols="6"
                      md="3"
                      sm="3"
                      class="text-center ma-0 px-3"
                      v-for="(item, index) in stats"
                      :key="index"
                    > 
                    <div style=" border-radius:12px;background-color: #FCEFBE;" class="pa-3">
                      <p style="font-size: 40px; font-weight: 600" class="mb-0">
                        {{ item.value }}
                      </p>
                      <p class="mb-0">{{ item.name }}</p>
                      </div>
                    </v-col>
                  </v-row>
                </v-container>

                <!-- <v-btn rounded outlined depressed large class="mt-5"
                  >See More</v-btn
                > -->
              <!-- </div> -->
            </v-col>
            <v-col md="5" class="pa-0">
              <v-img
                
                class="white--text align-end"
                style="border-radius:12px"
                src="https://raw.githubusercontent.com/GDG-Jalandhar/WebsiteData/master/events/devfest-jalandhar-2022/cabbana.jpeg"
              >
                <div class="ma-5">
                  <v-avatar color="white" size="32" class="mr-2">
                    <v-icon> mdi-google-maps </v-icon>
                  </v-avatar>
                  <!-- <v-chip color="#F4B400">The Cabbana Resort and Spa, Phagwara, Punjab, India</v-chip> -->
                  <v-chip color="#F4B400">The Cabbana Resort and Spa, Phagwara, Punjab</v-chip>
                </div>
              </v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "OverviewHome",
  data: () => ({
    stats: [
      {
        name: "Day",
        value: "01",
      },
      {
        name: "Attendee",
        value: "2000+",
      },
      {
        name: "Speakers",
        value: "30+",
      },
      {
        name: "Technologies",
        value: "9+",
      },
    ],
  }),
};
</script>

<style>
</style>