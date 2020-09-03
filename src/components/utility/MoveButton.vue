<template>
  <v-btn rounded @click="$vuetify.goTo(target)">{{ text }}</v-btn>
</template>

<script>
export default {
  props: {
      text: String,
      target: String,
  },
};
</script>