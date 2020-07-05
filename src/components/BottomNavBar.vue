<template>
  <v-footer padless>
    <v-col class="text-center" cols="12">
      <v-card color="transparent" elevation="0" flat tile class="mx-auto text-center">
        <v-card-text>
          <Contacts />
        </v-card-text>

        <v-card-text class="white--text pt-0">
          <p>kukkaniemi.riku@gmail.com</p>
          <p>{{ new Date().getFullYear() }} — <strong>Riku Kukkaniemi</strong></p>
        </v-card-text>
      </v-card>
    </v-col>
  </v-footer>
</template>

<script>
import Contacts from "./helpers/Contacts";

export default {
  components: {
    Contacts
  }
};
</script>