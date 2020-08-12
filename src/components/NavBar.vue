<template>
  <v-app-bar max-height="70" dense elevate-on-scroll>
    <v-tabs centered>
      <ContactDetails />
    </v-tabs>
  </v-app-bar>
</template>

<script>
import ContactDetails from "./ContactDetails";

export default {
  components: {
    ContactDetails,
  },
};
</script>
