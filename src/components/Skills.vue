<template>
  <div>
    <h2 class="text-center my-3">Osaaminen</h2>
    <HeaderUnderliner />
    <v-card class="mx-auto" max-width="300">
      <div v-for="(category, c) in skillCategory" :key="c">
        <v-list flat>
          <v-subheader>{{ c }}</v-subheader>
          <v-list-item-group>
            <v-list-item v-for="(language, l) in category" :key="l">
              <v-list-item-icon>
                <v-icon
                  :color="language.icon.color"
                  v-text="language.icon.code"
                ></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="language.text"></v-list-item-title>
              </v-list-item-content>
              <StarRating :rating="language.rating" />
            </v-list-item>
          </v-list-item-group>
        </v-list>
        <v-divider />
      </div>
    </v-card>
    <div class="text-center mt-5">
      <h3 class="mb-3">Selitykset tähdille:</h3>
      <p class="mb-5">
        <StarRating rating=3 />
        Päivittäisessä käytössä kehittynyt taito.
      </p>
      <p class="my-5">
        <StarRating rating=2 />
        Vahvaa osaamista taidosta, vaikkei olekaan päivittäisessä käytössä.
      </p>
      <p class="mt-5">
        <StarRating rating=1 />
        Opittu, mutta vähällä käytöllä ollut taito.
      </p>
    </div>
  </div>
</template>

<script>
import HeaderUnderliner from "./utility/HeaderUnderliner";
import StarRating from "./utility/StarRating";

export default {
  components: {
    HeaderUnderliner,
    StarRating,
  },
  data: () => ({
    skillCategory: {
      backend: [
        {
          icon: {
            color: "red",
            code: "mdi-laravel",
          },
          text: "Laravel",
          rating: 3,
        },
        {
          icon: {
            color: "blue",
            code: "mdi-language-php",
          },
          text: "PHP",
          rating: 3,
        },
        {
          icon: {
            color: "blue",
            code: "mdi-language-python",
          },
          text: "Python",
          rating: 1,
        },
      ],
      frontend: [
        {
          icon: {
            color: "green",
            code: "mdi-vuejs",
          },
          text: "Vue.js",
          rating: 2,
        },
        {
          icon: {
            color: "yellow",
            code: "mdi-language-javascript",
          },
          text: "JavaScript",
          rating: 2,
        },
        {
          icon: {
            color: "blue",
            code: "mdi-vuetify",
          },
          text: "Vuetify",
          rating: 2,
        },
      ],
    },
  }),
};
</script>