<template>
  <v-app>
    <NavBar />
    <v-main class="mx-md-10">
      <Introduction class="my-6" />
      <v-divider />
      <Skills class="my-6" />
      <v-divider />
      <Experience class="my-6" />
      <v-divider />
      <Education class="my-6" />
    </v-main>
    <BottomNavBar />
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Introduction from "./components/Introduction";
import Skills from "./components/Skills";
import Experience from "./components/Experience";
import Education from "./components/Education";
import BottomNavBar from "./components/BottomNavBar";

export default {
  components: {
    NavBar,
    Introduction,
    Skills,
    Experience,
    Education,
    BottomNavBar,
  }
};
</script>
