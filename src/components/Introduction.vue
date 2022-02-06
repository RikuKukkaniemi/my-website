<template>
  <div>
    <p class="text-center text-h4 my-3">Introduction</p>
    <HeaderUnderliner />
    <v-card elevation="0" color="transparent" class="text-center mx-auto" width="900px">
      <v-card-subtitle class="pb-10">
        <v-avatar size="200">
          <img src="../assets/face.png" alt="my picture" />
        </v-avatar>
      </v-card-subtitle>
      <v-card-text class="px-14">
        <div
          class="text--primary body-1"
        >I have worked in software development since 2018. Currently I feel like I'm at my strongest at backend development and designing. I also have some experience in frontend development with modern JavaScript frameworks.</div>
        <div class="text--primary mt-4 body-1">
          In coding I like to invest in quality and customization. I am used to manage the code quality by code reviews, unit testing and CI/CD-pipelines. In coding I try to follow
          <a href="https://en.wikipedia.org/wiki/SOLID" class="text-decoration-none">SOLID</a> architecture principles to help the applications to become as customizable as possible.
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
import HeaderUnderliner from "./utility/HeaderUnderliner";

export default {
  components: {
    HeaderUnderliner,
  },
};
</script>
