<template>
  <v-main>
    <v-container fluid class="">
      <v-row justify="center" align="center">
        <v-col md="12" sm="12" cols="12" lg="10" class="google-font">
          <v-container fluid>
            <v-row align="start" justify="start">
              <v-col md="11" lg="9" class="my-10">
                <p
                  class="google-font gdg-heading mb-0 grey--text text--darken-2"
                >
                  Jobs
                </p>
                <p>We've partnered with top companines to help our community members find jobs. Find the role that fits you best and apply</p>
                <!-- {{ jobs }} -->

                <v-data-table

                  :headers="headers"
                  :items="jobs"
                  :items-per-page="10"
                  class="elevation-0"
                  style="border:1px solid #e0e0e0;border-radius: 5px"
                  mobile-breakpoint="0"
                >
                <template v-slot:[`item.company`]="{ item }">
                      <a :href="item.company.link" target="_black">{{
                        item.company.name
                      }}</a>
                </template>

                <template v-slot:[`item.actions`]="{ item }">
                    <JobDialogeVue :item="item"/>
                </template>

              </v-data-table>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>
  
  <script>
import data from "../assets/data/jobs.json";
import JobDialogeVue from "../components/Common/JobDialoge.vue";

export default {
  name: "FAQComponent",
  components:{
    JobDialogeVue
  },
  data: () => ({
    jobs: data,
    headers: [
      {
        text: "Job Title",
        align: "start",
        sortable: false,
        value: "JobTitle",
      },
      { text: "Comapany", value: "company" },
      { text: "Experience", value: "JobExp" },
      { text: "Location", value: "JobLoc" },
      { text: "Actions", value: "actions" },
    ],
  }),
  created() {
    document.title = "Jobs | DevFest Jalandhar 2022";
  },
};
</script>
  
  <style scoped></style>
  