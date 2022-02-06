<template>
  <v-app>
    <NavBar />
    <v-main class="mx-md-10 mb-16">
      <section id="welcome">
        <Welcome class="mx-auto my-16 pb-16" />
      </section>

      <section id="introduction">
        <v-divider class="my-16" />
        <Introduction class="mx-auto pb-16" />
      </section>

      <section id="skills">
        <v-divider class="my-16" />
        <Skills class="mx-auto pb-16" />
      </section>

      <section id="projects">
        <v-divider class="my-16" />
        <Projects class="mx-auto pb-16" />
      </section>

    </v-main>
    <BottomNavBar />
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Welcome from "./components/Welcome";
import Introduction from "./components/Introduction";
import Skills from "./components/Skills";
import Projects from "./components/Projects.vue";
import BottomNavBar from "./components/BottomNavBar";

export default {
  components: {
    NavBar,
    Introduction,
    Skills,
    Projects,
    Welcome,
    BottomNavBar,
  },
};
</script>
