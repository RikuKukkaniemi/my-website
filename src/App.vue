<template>
  <v-app>
    <NavBar />
    <v-content class="mx-auto mt-12">
      <v-card class="mx-auto mt-12" outlined>
      <Introduction />
      </v-card>
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";
import Introduction from "./components/Introduction";

export default {
  components: {
    NavBar,
    Introduction,
  }
};
</script>
