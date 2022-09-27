<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="12" sm="12" cols="12" lg="10" class="google-font my-10">
          <v-container fluid>
            <v-row align="start" justify="start">
              <v-col md="11" lg="11">
                <v-container fluid>
                  <v-row justify="center" align="center">
                    <v-col md="8" order-md="1" order="2">
                      <p
                        class="
                          google-font
                          gdg-heading
                          mb-0
                          grey--text
                          text--darken-2
                        "
                      >
                        Help GDG Jalandhar
                      </p>
                      <p>
                        We try to engage developers, fresh graduates and
                        professionals through our events & meetups. The motive
                        is to create a local ecosystem of programmers &
                        developers in and around Jalandhar. The technology
                        awareness is main goal for first few years of the group.
                      </p>
                      <p>
                        To put it in a nutshell, we are a community that
                        organizes tech talks, workshops, bootcamps, Google
                        flagship events where programmers meet to discuss and
                        work with several Google developer resources and
                        products.
                      </p>
                      <v-chip dark color="#4285F4"
                        >Donate Us via Scan the QR Code</v-chip
                      >
                    </v-col>
                    <v-col md="4" order-md="2" order="1" class="text-center">
                      <v-img
                        style="border-radius: 12px"
                        :src="require('@/assets/img/qrcode.jpeg')"
                      ></v-img>
                      <p class="mt-4 mb-0">Scan the QR Code to Donate</p>
                    </v-col>
                  </v-row>
                </v-container>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>
  
  <script>
export default {
  name: "CoCComponent",
  data: () => ({}),
  created() {
    document.title = "Donate | DevFest Jalandhar 2022";
  },
};
</script>
  
  <style scoped></style>
  