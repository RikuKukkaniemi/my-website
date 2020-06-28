<template>
  <v-app>
    <NavBar />
    <v-content >
      <Introduction class="my-6" />
      <v-divider />
      <Skills class="mt-6" />
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Introduction from "./components/Introduction";
import Skills from "./components/Skills";

export default {
  components: {
    NavBar,
    Introduction,
    Skills,
  }
};
</script>
