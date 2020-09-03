<template>
  <v-card elevation="0" color="transparent" class="mx-auto text-center">
    <v-card-subtitle class="headline text--primary">Tervetuloa sivuilleni!</v-card-subtitle>
    <v-card-actions class="mt-6">
      <v-spacer />
      <MoveButton text="Esittely" target="#introduction" />
      <MoveButton text="Osaaminen" target="#skills" />
      <MoveButton text="Työkokemus" target="#experience" />
      <MoveButton text="Koulutus" target="#education" />
      <v-spacer />
    </v-card-actions>
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
