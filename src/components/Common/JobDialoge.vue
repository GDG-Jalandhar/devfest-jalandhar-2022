<template>
  <v-dialog v-model="dialog" width="900" scrollable>
    <template v-slot:activator="{ on, attrs }">
      <v-btn v-on="on" outlined v-bind="attrs" small>More Info</v-btn>
    </template>
    <v-card class="white google-font" v-if="dialog" style="border-radius: 12px">
      <v-card-text class="pa-0">
        <v-container fluid class="py-8">
          <v-row>
            <v-col md="12" cols="12" class="px-md-10 px-5">
              <p>
                <a :href="item.company.link" target="_black">{{
                  item.company.name
                }}</a>
              </p>
              <p class="mb-1" style="font-size: 28px">{{ item.JobTitle }}</p>
              <p>{{ item.JobType }} | {{ item.JobExp }} | {{ item.JobLoc }}</p>

              <v-btn
                :href="item.ApplyLink"
                target="_blank"
                color="#4285F4"
                dark
                depressed
                right
              >
                Apply Now
              </v-btn>

              <!-- <p style="font-size: 200%">{{ item.name }}</p> -->

              <p class="mt-4" style="font-size: 16px" v-html="item.JobDesc"></p>
            
            <div v-if="item.EligibilityCriteria.length">
              <p class="mb-0" style="font-size: 17px; color: black">
                <b>Eligibility Criteria</b>
              </p>
              <p
                class="mt-0"
                style="font-size: 16px"
                v-html="item.EligibilityCriteria"
              ></p>
            </div>

              <p class="mb-0" style="font-size: 17px; color: black">
                <b>Technical Skills</b>
              </p>
              <p
                class="mt-0"
                style="font-size: 16px"
                v-html="item.JobSkills"
              ></p>

              <p class="mb-0" style="font-size: 17px; color: black">
                <b>Selection Process</b>
              </p>
              <p
                class="mt-0"
                style="font-size: 16px"
                v-html="item.SelectionProcess"
              ></p>

              <v-btn
                :href="item.ApplyLink"
                target="_blank"
                color="#4285F4"
                dark
                depressed
                right
              >
                Apply Now
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-card-text>

      <!-- <v-divider></v-divider> -->

      <v-card-actions class="white">
        <v-spacer></v-spacer>
        <v-btn aria-label="close" class="px-10" text @click="dialog = false"
          >Close</v-btn
        >
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>
    
    <script>
export default {
  props: ["item"],
  data: () => ({
    dialog: false,
  }),
  methods: {},
};
</script>
    
    <style>
</style>