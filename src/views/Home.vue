<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <v-img
      dark
      max-height="500px"
      src="https://images.unsplash.com/photo-1505238680356-667803448bb6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div class="display-2 font-weight-bold">Welcome to my portfolio.</div>
              <div class="headline">I'm a multimediedesigner student.</div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="mt-5">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="about">This is me</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{aboutText}}</div>
          <div
            class="body-1 mt-3"
          ></div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="portfolio">My Work</div>
        </v-flex>

              
          
        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(app, i) in apps">
              <v-flex :key="i" xs12 sm6 md4>
                <p-portfolio-app :app="app" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="contact">Send me a message.</div>
        </v-flex>
        <template v-for="(contact, i) in contactLinks">
          <v-flex sm6 md4 xs12 :key="i">
            <p-contact-info :contact="contact" />
          </v-flex>
        </template>
      </v-layout>
      
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import PPortfolioApp from "@/components/PPortfolioApp.vue";
import PContactInfo from "@/components/PContactInfo.vue";

export default {
  name: "home",
  components: {
    // HelloWorld,
    PPortfolioApp,
    PContactInfo
  },
  data() {
    return {
      aboutText:
        "My name is Daniel Olesen and i am 21 year old.",
      
      contactLinks: [
        {
          name: "Email",
          value: "danielolesen0@gmail.com",
          link: "mailto:danielolesen0@gmail.com",
          icon: "mdi-email"
        },
        {
          name: "LinkedIn",
          value: "Daniel Olesen",
          link: "https://www.linkedin.com/in/daniel-olesen-71b2521a1/",
          icon: "mdi-linkedin"
        },
        {
          name: "YouTube",
          value: "Daniel Olesen",
          link: "https://www.youtube.com/channel/UCtyAOdRMQHYZc3DR3M197vQ/featured?view_as=subscriber",
          icon: "mdi-youtube"
        },
        {
          name: "Github",
          value: "mormormorfar",
          link: "https://github.com/mormormorfar",
          icon: "mdi-github-circle"
        },
        {
          name: "Facebook",
          value: "Daniel Olesen",
          link: "https://www.facebook.com/daniel.olesen.75",
          icon: "mdi-facebook"
        },
       
          <button onclick="runcode()">click me</button>
          
      
        
      ]
    };
  }
};
</script>
