<template>
  <v-btn class="align-self-end" fab outlined @click="$vuetify.goTo(target)">
    <v-icon>mdi-chevron-double-down</v-icon>
  </v-btn>
</template>

<script>
export default {
  props: {
      target: String,
  },
};
</script>
