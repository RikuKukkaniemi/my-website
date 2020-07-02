<template>
  <v-app>
    <NavBar />
    <v-content >
      <Introduction class="my-6" />
      <v-divider />
      <Skills class="my-6" />
      <v-divider />
      <Experience class="my-6" />
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Introduction from "./components/Introduction";
import Skills from "./components/Skills";
import Experience from "./components/Experience";

export default {
  components: {
    NavBar,
    Introduction,
    Skills,
    Experience,
  }
};
</script>
