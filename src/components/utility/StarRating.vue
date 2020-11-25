<template>
  <v-rating
    length="3"
    size="20"
    :value="rating"
    readonly
    dense
    color="yellow"
    background-color="yellow lighten-3"
  ></v-rating>
</template>

<script>
export default {
  props: {
    rating: Number,
  },
};
</script>