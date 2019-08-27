<template>
  <v-layout column justify-center align-center>
    <h1 class="text-center headline mb-6 myFont">My Work</h1>
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-row align justify="center" style="height: 300px">
          <Project
            :image="thing.image"
            :description="thing.description"
            :github="thing.github"
            :project="thing.project"
            v-for="(thing, i) in things"
            :key="i"
          ></Project>
        </v-row>
      </v-row>
    </v-container>
  </v-layout>
</template>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto+Mono&display=swap");
.myWrap {
  overflow-wrap: break-word;
}
</style>

<script>
import Project from "~/components/Project.vue";

export default {
  components: { Project },
  computed: {},
  // methods: {
  //   getImg(path) {
  //     return require(path);
  //   }
  // },
  data() {
    return {
      hover: true,
      things: [
        {
          image:
            "https://storage.googleapis.com/twitch0125-portfolio/burgers.jpg",
          description:
            "This was my first 'From Scratch' website. No fancy shmancy framework was used, just plain HTML, CSS, and a little JS.",
          github: "https://github.com/Twitch0125/burgersite",
          project: "https://twitch0125.github.io/burgersite/"
        },
        {
          image: "https://storage.googleapis.com/twitch0125-portfolio/chat.png",
          description:
            "With my chat app, I experimented with Socket.IO and Express. This was to begin learning NodeJS and writing server-side code.",
          github: "https://github.com/Twitch0125/chat-server-and-client"
        },
        {
          image:
            "https://storage.googleapis.com/twitch0125-portfolio/ecommerce.png",
          description:
            "This was my first dive into a web app framework(or library if you wanna be specific). I used React combined with Axios, Redux, and Material UI",
          github: "https://github.com/Twitch0125/ecommerce",
          project: "https://twitch0125.github.io/ecommerce/"
        },
        {
          image:
            "https://storage.googleapis.com/twitch0125-portfolio/golfscorecard.png",
          description:
            "The purpose of my Golf Score Card was to really get a grip on JavaScript and jQuery, I also used Material Design Lite for styles. Currently, I'm in the process of remaking this in Angular",
          github: "https://github.com/Twitch0125/golfscorecard",
          project: "https://twitch0125.github.io/golfscorecard/"
        },
        {
          image:
            "https://storage.googleapis.com/twitch0125-portfolio/todoapp.png",
          description:
            "This was when I was just starting to learn JavaScript. I used Material Design Lite for the styling.",
          github: "https://github.com/Twitch0125/todoApp",
          project: "https://twitch0125.github.io/todoApp/"
        },
        {
          image:
            "https://storage.googleapis.com/twitch0125-portfolio/userManager.png",
          description:
            "My User Manager I made while I was learning App Deployment(AWS, Docker), and Databases. There are 2 variants, one that uses MongoDB(on Mongo Atlas), and one that uses PostgreSQL (hosted on Heroku). This is a server-side rendered app, using PugJS(prev. Jade) I also made a dockerimage of the Mongo user manager",
          github: "https://github.com/Twitch0125/user-manager-postgresql",
          project: "https://enigmatic-forest-13135.herokuapp.com/"
        }
      ]
      // images: [
      //   { url: "../assets/burgers.jpg" },
      //   { url: "../assets/chat.png" },
      //   { url: "../assets/ecommerce.png" },
      //   { url: "../assets/golfscorecard.png" },
      //   { url: "../assets/todoapp.png" },
      //   { url: "../assets/userManager.png" }
      // ]
    };
  }
};
</script>
