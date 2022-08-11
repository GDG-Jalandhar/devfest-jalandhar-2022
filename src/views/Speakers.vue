<template>
  <v-main>
    <v-container fluid>
      <v-row justify="center" align="center">
        <v-col md="11" sm="11" lg="11" class="google-font my-15 py-10">
          <v-container fluid>
            <!-- Heading -->
            <v-row justify="center" align="center">
              <v-col>
                <p class="super-heading">Speakers</p>
                <p style="font-size:20px">
                  Interested in Android, Flutter, Web, Cloud, ML technologies?
                  <br>
                  Join the vibrant and divrse set of speakers where you can
                  learn, network, share knowledge and enjoy the experience.
                </p>
              </v-col>
            </v-row>
            <!-- Heading -->

            <!-- Speaker Cards -->
            <v-row justify="start" align="start">
                <v-col
                md="3"
                lg="2"
                xl="2"
                sm="4"
                cols="6"
                class="px-1"
                v-for="(item, index) in SpeakersData"
                :key="index"
              >
                <SpeakerDialog :speakerData="item" :SessionDetails="SessionDetails" />
              </v-col>
            </v-row>
            <!-- Speaker Cards -->
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
import SpeakersDataTemp from "@/assets/data/speakers.json";
import SessionDetails from "@/assets/data/sessions.json";
export default {
  name: "SpeakersComponent",
  components: {
    SpeakerDialog: () => import("../components/Speakers/SpeakerDialog.vue"),
  },
  data: () => ({
    SpeakersData: [],
  }),
  created(){
    document.title = 'Speakers | DevFest Jalandhar'
  },
  mounted() {
    this.SpeakersData = this.sortByName(SpeakersDataTemp);
    this.SessionDetails = SessionDetails.sort((a, b) => {
      return a.id > b.id ? 1 : -1;
    });
  },
};
</script>

<style lang="scss" scoped></style>
