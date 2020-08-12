<template>
  <v-app>
    <NavBar />
    <v-content class="mx-md-10">
      <section id="introduction">
        <Introduction class="mx-auto" />
        <v-row align="center" class="mx-auto" justify="center">
          <DownButton target="#skills" />
        </v-row>
      </section>

      <v-divider class="my-6" />

      <section id="skills">
        <v-row align="center" class="mx-auto" justify="center">
          <UpButton target="#introduction" />
        </v-row>
        <Skills class="my-6" />
        <v-row align="center" class="mx-auto" justify="center">
          <DownButton target="#experience" />
        </v-row>
      </section>

      <v-divider class="my-6" />

      <section id="experience">
        <v-row align="center" class="mx-auto" justify="center">
          <UpButton target="#skills" />
        </v-row>
        <Experience class="my-6" />
        <v-row align="center" class="mx-auto" justify="center">
          <DownButton target="#education" />
        </v-row>
      </section>

      <v-divider class="my-6" />

      <section id="education">
        <v-row align="center" class="mx-auto" justify="center">
          <UpButton target="#experience" />
        </v-row>
        <Education class="my-6" />
      </section>
    </v-content>
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
import DownButton from "./components/utility/DownButton";
import UpButton from "./components/utility/UpButton";

export default {
  components: {
    NavBar,
    Introduction,
    Skills,
    Experience,
    Education,
    BottomNavBar,
    DownButton,
    UpButton,
  },
};
</script>
