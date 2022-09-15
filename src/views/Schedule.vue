<template>
  <v-main>
    <v-container fluid>
      <v-row justify="center" align="center">
        <v-col md="11" sm="11" lg="11" class="google-font my-15 py-10">
          <!-- Page Content -->
          <v-container fluid>
            <!-- Heading -->
            <v-row justify="center" align="center">
              <v-col>
                <p class="super-heading">Schedule</p>
                <p style="font-size:20px">
                  Follow code demonstrations by our expert speakers on 5
                  different tracks. Check out the schedule below and don't
                  forget to mark your calendar so that you don't miss out on any
                  sessions.
                </p>
                <!-- style="width:100%;border-bottom:1px solid #e0e0e0" -->
                <v-toolbar flat class="px-0">
                  <v-tabs
                    v-model="model"
                    color="primary"
                    slider-color="primary"
                  >
                    <v-tab href="#day1">Day 1</v-tab>
                    <v-tab href="#day2">Day 2</v-tab>
                    <v-tab href="#day3">Day 3</v-tab>
                  </v-tabs>
                </v-toolbar>
              </v-col>
            </v-row>
            <!-- Heading -->

            <!-- Schedule Tab Content -->
            <v-row justify="center" align="center">
                <v-col>
                    <v-tabs-items v-model="model">
                        <v-tab-item value="day1">
                            <!-- <p class="h1-heading">Day 1 Schdule</p>
                            <p class="h1-subheading">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore provident maiores et pariatur illum quis enim nam labore deserunt voluptate! Amet hic voluptate ad? Sed, eius laudantium. Quo, voluptate inventore!</p> -->
                            <ScheduleDetails :data="ScheduleData[0]" />
                        </v-tab-item>
                        <v-tab-item value="day2">
                            <!-- <p class="h1-heading">Day 2 Schdule</p>
                            <p class="h1-subheading">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore provident maiores et pariatur illum quis enim nam labore deserunt voluptate! Amet hic voluptate ad? Sed, eius laudantium. Quo, voluptate inventore!</p> -->
                            <ScheduleDetails :data="ScheduleData[1]" />
                        </v-tab-item>
                        <v-tab-item value="day3">
                            <p class="h1-heading">Day 3 Schdule</p>
                            <p class="h1-subheading">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Inventore provident maiores et pariatur illum quis enim nam labore deserunt voluptate! Amet hic voluptate ad? Sed, eius laudantium. Quo, voluptate inventore!</p>
                            <ScheduleDetails :data="ScheduleData[2]" />
                        </v-tab-item>
                    </v-tabs-items>
                </v-col>
            </v-row>
            <!-- Schedule Tab Content -->
          </v-container>
          <!-- Page Content -->
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
import ScheduleDetailsData from "@/assets/data/schedule.json";
import ScheduleDetails from "@/components/Schedule/ScheduleDetails";
export default {
  name: "ScheduleComponent",
  components:{
    ScheduleDetails
  },
  data: () => ({
    model: "day1",
    ScheduleData: [],
  }),
  created(){
    document.title = 'Schedule | DevFest Jalandhar 2022'
  },
  mounted(){
    let tabs = ['day1','day2','day3']
    if (Object.keys(this.$route.query) == "tab"){
        if(tabs.indexOf(this.$route.query["tab"])!=-1){
            this.model = this.$route.query["tab"]
        }
    }
    this.ScheduleData = ScheduleDetailsData;
  }
};
</script>

<style scoped>
    .v-toolbar__content{
        padding: 0;
    }
</style>
