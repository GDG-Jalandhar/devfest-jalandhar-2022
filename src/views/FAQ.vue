<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="11" sm="11" lg="11" class="google-font my-15 py-10">
          <v-container fluid>
            <v-row align="start" justify="start">
              <v-col md="11" lg="9">
                <p class="mb-0 super-heading">Frequently asked questions</p>
                <p class="my-0 mb-8 h1-subheading">
                  Need Answers? Everything you need to know
                </p>
                <v-expansion-panels flat accordion class="">
                  <v-expansion-panel
                    v-for="(faq, i) in faqsData"
                    :key="i"
                    class="px-0 mx-0"
                    style="border-bottom:1px solid #e0e0e0"
                  >
                    <v-expansion-panel-header class="">
                      <p
                        class="google-font"
                        style="font-size:125%;margin:auto;"
                      >
                        {{ faq.question }}
                      </p>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content class="grey lighten-4">
                      <p
                        class="google-font text-left my-0 mt-5"
                        style="font-size:110%;"
                        v-html="faq.answer"
                      ></p>
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                </v-expansion-panels>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
import data from "../assets/data/faq.json";
export default {
  name: "FAQComponent",
  data: () => ({
    faqsData: data,
  }),
  created(){
    document.title = 'FAQ | DevFest India'
  }
};
</script>

<style scoped></style>
