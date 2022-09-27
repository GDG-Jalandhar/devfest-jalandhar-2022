<template>
  <v-container fluid id="support">
    <v-row justify="center" align="center"> 
      <v-col
        cols="12"
        md="8"
        class="grey lighten-4 pa-8"
        style="border-radius: 12px"
      >
        <v-container fluid>
          <v-row justify="center" align="center">
            <v-col md="7">
              <p
                
                class="google-font gdg-h1 mb-0 grey--text text--darken-2"
              >
                Help GDG Jalandhar
              </p>
              <p>
                We try to engage developers, fresh graduates and professionals through our events & meetups. The motive is to create a local ecosystem of programmers & developers in and around Jalandhar. The technology awareness is main goal for first few years of the group.
              </p>
              <p>To put it in a nutshell, we are a community that organizes tech talks, workshops, bootcamps, Google flagship events where programmers meet to discuss and work with several Google developer resources and products.</p>
              <v-chip dark color="#4285F4">Donate Us</v-chip>
            </v-col>
            <v-col md="5" class="text-center">
                <v-img style="border-radius:12px" :src="require('@/assets/img/qrcode.jpeg')"></v-img>
                <p class="mt-4 mb-0">Scan the QR Code to Donate</p>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
      <v-col
        cols="12"
        md="4"
    
        style="border-radius: 12px">
        <v-img style="border-radius:12px" :src="require('@/assets/img/team.jpeg')"></v-img>
    </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
export default {};
</script>
  
  <style>
</style>