<template>
  <v-card elevation="0" color="transparent" class="mx-auto text-center">
    <v-card-subtitle class="text--primary text-h2">Hi there!</v-card-subtitle>
    <v-card-subtitle class="text--primary text-h5 pa-1">My name is Riku and I'm a software developer.</v-card-subtitle>
    <v-card-subtitle class="text--primary text-h5 pa-1">Welcome to my website!</v-card-subtitle>
    <v-card-text class="mt-6">
      <v-spacer />
      <MoveButton class="ma-2" text="Introduction" target="#introduction" />
      <MoveButton class="ma-2" text="Skills" target="#skills" />
      <MoveButton class="ma-2" text="Projects" target="#projects" />
      <v-spacer />
    </v-card-text>
  </v-card>
</template>

<script>
import MoveButton from "./utility/MoveButton";

export default {
  components: {
    MoveButton,
  },
};
</script>
