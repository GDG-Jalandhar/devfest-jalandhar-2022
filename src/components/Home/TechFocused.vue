<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <p class="google-font gdg-h1 mb-0 grey--text text--darken-2">
          Technologies to be focused
        </p>
        <p>
          At sessions that span from the technical to the visionary, let’s
          celebrate and discover what the technologies can enable: how product
          innovation, open source, and ML and AI can propel enterprises forward
          and solve the big problems that impact all of us.
        </p>

        <v-container fluid>
          <v-row justify="start" align="start">
            <v-col md="1" sm="2" v-for="(item, index) in techs" :key="index">
              <a :href="item.link" target="_blank">
                <v-avatar color="grey" class="lighten-4" size="80">
                  <v-img :src="item.logo"></v-img>
                </v-avatar>
              </a>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    techs: [
      {
        name: "Android",
        link: "https://developer.android.com/",
        logo: "https://io.google/2022/app/images/android-logo.svg",
      },
      {
        name: "Chrome OS",
        link: "https://chromeos.dev/en",
        logo: "https://io.google/2022/app/images/chrome-logo.svg",
      },
      {
        name: "Firebase",
        link: "https://firebase.google.com/",
        logo: "https://io.google/2022/app/images/firebase-logo.svg",
      },
      {
        name: "Flutter",
        link: "https://flutter.dev/",
        logo: "https://io.google/2022/app/images/flutter-logo.svg",
      },
      {
        name: "Google Assistant & Smart Home",
        link: "https://developers.google.com/assistant",
        logo: "https://io.google/2022/app/images/googleassistant-logo.svg",
      },
      {
        name: "Google Cloud",
        link: "https://cloud.google.com/",
        logo: "https://io.google/2022/app/images/googlecloud-logo.svg",
      },
      {
        name: "Google Maps",
        link: "https://developers.google.com/maps",
        logo: "https://io.google/2022/app/images/googlemaps-logo.svg",
      },
      {
        name: "TensorFlow",
        link: "https://www.tensorflow.org/",
        logo: "https://io.google/2022/app/images/machinelearning-logo.svg",
      },
      {
        name: "Web",
        link: "https://developers.google.com/web",
        logo: "https://io.google/2022/app/images/web-logo.svg",
      },
    ],
  }),
};
</script>

<style>
</style>