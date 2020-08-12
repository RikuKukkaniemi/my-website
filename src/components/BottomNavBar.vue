<template>
  <v-footer padless>
    <v-col class="text-center" cols="12">
      <v-card color="transparent" elevation="0" flat tile class="mx-auto text-center">
        <v-card-text>
          <ContactDetails />
        </v-card-text>

        <v-card-text class="white--text pt-0">
          <p>
            {{ new Date().getFullYear() }} —
            <strong>Riku Kukkaniemi</strong>
          </p>
        </v-card-text>
      </v-card>
    </v-col>
  </v-footer>
</template>

<script>
import ContactDetails from "./ContactDetails";

export default {
  components: {
    ContactDetails
  }
};
</script>