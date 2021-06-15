<template>
  <v-card elevation="0" color="transparent" class="mx-auto text-center">
    <v-card-subtitle class="text--primary text-h2">Moi!</v-card-subtitle>
    <v-card-subtitle class="text--primary text-h5 pa-1">Nimeni on Riku ja olen sovelluskehittäjä.</v-card-subtitle>
    <v-card-subtitle class="text--primary text-h5 pa-1">Tervetuloa sivuilleni!</v-card-subtitle>
    <v-card-text class="mt-6">
      <v-spacer />
      <MoveButton class="ma-2" text="Esittely" target="#introduction" />
      <MoveButton class="ma-2" text="Osaaminen" target="#skills" />
      <MoveButton class="ma-2" text="Työkokemus" target="#experience" />
      <MoveButton class="ma-2" text="Koulutus" target="#education" />
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
