<template>
  <v-app>
    <NavBar />
    <v-content class="mx-md-10 mb-16">
      <section id="welcome">
        <Welcome class="mx-auto my-16 pb-16" />
      </section>

      <section id="introduction">
        <v-divider class="my-16" />
        <Introduction class="mx-auto pb-16" />
      </section>

      <section id="skills">
        <v-divider class="my-16" />
        <Skills class="pb-16" />
      </section>

      <section id="experience">
        <v-divider class="my-16" />
        <Experience class="pb-16" />
      </section>

      <section id="education">
        <v-divider class="my-16" />
        <Education class="pb-16" />
      </section>
    </v-content>
    <BottomNavBar />
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Welcome from "./components/Welcome";
import Introduction from "./components/Introduction";
import Skills from "./components/Skills";
import Experience from "./components/Experience";
import Education from "./components/Education";
import BottomNavBar from "./components/BottomNavBar";

export default {
  components: {
    NavBar,
    Introduction,
    Welcome,
    Skills,
    Experience,
    Education,
    BottomNavBar,
  },
};
</script>
