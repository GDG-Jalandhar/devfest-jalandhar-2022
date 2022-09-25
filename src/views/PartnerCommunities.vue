<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="12" sm="12" cols="12" lg="10" class="google-font my-10">
          <v-container fluid>
            <v-row align="start" justify="start">
              <v-col md="11" lg="11">
                <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">
                  Our Community Partners
                </p>
                <!-- <p>Sponsors dedicated to building remarkable experience!</p> -->
              </v-col>
            </v-row>
            <v-row class="pa-0 ma-0" justify="start" align="start">
              <v-col
              lg="3"
              md="3"
              sm="4"
              cols="12"
                class="px-1"
                v-for="(item, index) in pc"
                :key="index"
              >
                <PartnerDialogeVue :item="item" />
                
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>
  
  <script>
    import partnerData from '../assets/data/partner.json'
    import PartnerDialogeVue from '../components/Common/PartnerDialoge.vue';
export default {
  name: "PCComponent",
  components: { PartnerDialogeVue },
  data: () => ({
    pc: partnerData
  }),
  created() {
    document.title = "Community Partner | DevFest Jalandhar 2022";
  },
};
</script>
  
  <style scoped></style>
  