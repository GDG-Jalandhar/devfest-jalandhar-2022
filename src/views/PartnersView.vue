<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="12" sm="12" cols="12" lg="10" class="google-font my-10">
          <v-container fluid>
            <v-row>
              <v-col md="12" class="text-center">
                <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">
                  Sponsors
                </p>
                <p>Sponsors dedicated to building remarkable experience!</p>
                <v-btn
                  depressed
                  rounded
                  color="#4285F4"
                  dark
                  href="https://bit.ly/dfj-22-sponsorship-form"
                  target="_blank"
                  class="mx-1 mt-1"
                  >Become a Sponsor</v-btn
                >
                <v-btn
                  depressed
                  rounded
                  color="#4285F4"
                  target="_blank"
                  href="https://bit.ly/dfj-22-sponsorship-brochure"
                  outlined
                  class="mx-1 mt-1"
                  >Sponsorship Brochure</v-btn
                >
              </v-col>
            </v-row>

            <v-row class="" justify="center" align="center">
              <v-col md="12" class="text-center">
                
                <v-container fluid class="py-0 my-0">
                  <v-row align="center" justify="center" class="">
                    <v-col md="4" class="">
                      <SponsorDialogeVue
                        :item="{
                          img: 'https://www.gstatic.com/devrel-devsite/prod/vdb149cdc08c87ab249cdebfec6395e8f073056d752ca9c2d285d3b8426fcfa32/developers/images/lockup.svg',
                          name: 'Google Developer',
                          desc: `Google Developers is Google's site for software development tools and platforms, application programming interfaces, and technical resources. The site contains documentation on using Google developer tools and APIs—including discussion groups and blogs for developers using Google's developer products.`,
                          link: 'https://developers.google.com',
                        }"
                      />
                    </v-col>
                  </v-row>
                </v-container>

                <p class="google-font mt-10 mb-n2">Platinum Sponsors</p>
                <v-container fluid>
                  <v-row align="center" justify="center">
                    <v-col md="2">
                      <SponsorDialogeVue
                        :item="{
                          img: 'https://theme.zdassets.com/theme_assets/9442057/efc3820e436f9150bc8cf34267fff4df052a1f9c.png',
                          name: 'Stream',
                          desc: `Stream's <a href='https://getstream.io/chat/sdk/android/?utm_source=DevFest&utm_medium=Whole_Event_L&utm_content=Developer&utm_campaign=DevFest_October2022_AndroidChatSDK_klmh22'>Android</a> & <a href='https://getstream.io/chat/sdk/flutter/?utm_source=DevFest&utm_medium=Whole_Event_L&utm_content=Developer&utm_campaign=DevFest_October2022_FlutterChatSDK_klmh22'>Flutter</a> SDKs launch chat faster and its UI components make it easy to customize. Try it for free today!`,
                          link: 'https://getstream.io/chat/sdk/android/?utm_source=DevFest&utm_medium=Whole_Event_L&utm_content=Developer&utm_campaign=DevFest_October2022_AndroidChatSDK_klmh22',
                        }"
                      />
                    </v-col>
                  </v-row>
                </v-container>


                <p class="google-font mt-10 mb-n2">Hiring Partners</p>
                <v-container fluid>
                  <v-row align="center" justify="center">
                    <v-col md="2">
                      <SponsorDialogeVue
                        :item="{
                          img: 'https://raw.githubusercontent.com/GDG-Jalandhar/WebsiteData/master/partners/Cybertron.jpg',
                          name: 'Cybertron Technologies',
                          desc: `We are a Mobile App and  Website Development Firm based in Mohali, India. We provide programming services to multiple clients throughout the globe. Our team has skills in Angular, React, Node.js, Kotlin, Python, Laravel, Shopify, MySQL/Postgres/MongoDB etc. We are good at Expression Engine, WordPress, CakePHP, Bootstrap, SASS and jQuery. We also develop mobile apps and PWAs in the Ionic/Capacitor framework. In the past, we have worked with clients like Disney, Philips, MIT, Harvard University, American Pharmacists Association and Monash University.`,
                          link: 'https://www.cybertrontechnologies.com/',
                        }"
                      />
                    </v-col>
                  </v-row>
                </v-container>

                <p class="google-font mt-10 mb-n2">Knowledge Partners</p>
                <v-container fluid>
                  <v-row align="center" justify="center">
                    <v-col md="2">
                      <SponsorDialogeVue
                        :item="{
                          img: 'https://raw.githubusercontent.com/GDG-Jalandhar/WebsiteData/master/partners/dcc2.png',
                          name: 'Data Center on Cloud',
                          desc: `Data Center On Cloud is place where you will learn the fundamentals to advance concepts of hosting your application on Public Cloud Platforms.This idea behind this channel is to provide you the guidance to migrate your application which can be Web Apps, Databases, Business Applications, Hybrid Cloud, Multi Cloud etc. There will be special focus on Cloud Certification preparations. DC on Cloud is covering all the major Cloud Platforms available in market. If you are looking to start your learning or planning to appear for Amazon Web Services, Microsoft Azure, Google Cloud Platforms exams, Dc On Cloud is providing the content for the same.`,
                          link: 'https://www.youtube.com/c/DataCenterOnCloud/',
                        }"
                      />
                    </v-col>
                  </v-row>
                </v-container>
              </v-col>
            </v-row>

            <v-row justify="center" align="center" class="my-md-10 my-5">
              <v-col md="12">
                <v-divider></v-divider>
              </v-col>
            </v-row>

            <!-- Community -->
            <v-row class="" align="center" justify="center">
              <v-col md="11" lg="11" class="text-center">
                
                <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">
                  Community Partners
                </p>
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
import SponsorDialogeVue from "../components/Common/SponsorDialoge.vue";
import partnerData from "../assets/data/partner.json";
import PartnerDialogeVue from "../components/Common/PartnerDialoge.vue";
export default {
  name: "PCComponent",
  components: { PartnerDialogeVue, SponsorDialogeVue },
  data: () => ({
    pc: partnerData,
    pastEvents: [
      {
        title: "Google Developers",
        size: "250px",
        image:
          "https://www.gstatic.com/devrel-devsite/prod/vdb149cdc08c87ab249cdebfec6395e8f073056d752ca9c2d285d3b8426fcfa32/developers/images/lockup.svg",
        link: "https://developers.google.com/",
      },
    ],
  }),
  created() {
    document.title = "Community Partner | DevFest Jalandhar 2022";
  },
};
</script>
  
  <style scoped></style>
  