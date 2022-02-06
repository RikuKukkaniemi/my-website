<template>
  <div>
    <h2 class="text-center my-3">Skills</h2>
    <HeaderUnderliner />
    <div class="justify-center" :class="$vuetify.breakpoint.lgAndUp ? 'd-flex' : ''">
      <v-card
        v-for="(category, c) in skillCategory"
        :key="c"
        class="ma-3"
        max-width="300"
        :class="$vuetify.breakpoint.mdAndDown ? 'mx-auto' : ''"
      >
        <v-list flat>
          <v-subheader>{{ c }}</v-subheader>
          <v-list-item-group>
            <v-list-item v-for="(language, l) in category" :key="l">
              <v-list-item-icon>
                <v-icon :color="language.icon.color" v-text="language.icon.code"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="language.text"></v-list-item-title>
              </v-list-item-content>
              <StarRating class="ml-3" :rating="parseInt(language.rating)" />
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-card>
    </div>
    <div class="text-center mt-5">
      <h3 class="mb-3">Explanation for stars:</h3>
      <p class="mb-5">
        <StarRating :rating="parseInt(3)" />I have used this alot in work environment.
      </p>
      <p class="my-5">
        <StarRating :rating="parseInt(2)" />I have used this alot but only a little or not at all in work environment.
      </p>
      <p class="mt-5">
        <StarRating :rating="parseInt(1)" />This is still in learning or it has been a while since last time used.
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
      Backend: [
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
            color: "white",
            code: "mdi-symfony",
          },
          text: "Symfony",
          rating: 3,
        },
        {
          icon: {
            color: "indigo",
            code: "mdi-database",
          },
          text: "MySQL",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-api",
          },
          text: "RESTful APIs",
          rating: 3,
        },
        {
          icon: {
            color: "cyan",
            code: "mdi-language-go",
          },
          text: "Go",
          rating: 1,
        },
        {
          icon: {
            color: "amber",
            code: "mdi-language-java",
          },
          text: "Java",
          rating: 1,
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
      Frontend: [
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
        {
          icon: {
            color: "red",
            code: "mdi-angular",
          },
          text: "Angular",
          rating: 1,
        },
        {
          icon: {
            color: "cyan",
            code: "mdi-react",
          },
          text: "React",
          rating: 1,
        },
      ],
      DevOps: [
        {
          icon: {
            color: "blue",
            code: "mdi-docker",
          },
          text: "Docker",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-infinity",
          },
          text: "CI/CD",
          rating: 3,
        },
        {
          icon: {
            color: "blue",
            code: "mdi-kubernetes",
          },
          text: "Kubernetes",
          rating: 2,
        },
        {
          icon: {
            color: "deep-orange",
            code: "mdi-google-cloud",
          },
          text: "GCP",
          rating: 2,
        },
      ],
      Other: [
        {
          icon: {
            color: "deep-orange",
            code: "mdi-git",
          },
          text: "GIT",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-drawing",
          },
          text: "UML",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-hexagon-multiple",
          },
          text: "Microservices",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-developer-board",
          },
          text: "Kanban",
          rating: 3,
        },
        {
          icon: {
            color: "white",
            code: "mdi-developer-board",
          },
          text: "Scrum",
          rating: 3,
        },
        {
          icon: {
            color: "grey",
            code: "mdi-apple",
          },
          text: "MacOS",
          rating: 3,
        },
        {
          icon: {
            color: "blue",
            code: "mdi-microsoft-windows",
          },
          text: "Windows",
          rating: 2,
        },
      ],
    },
  }),
};
</script>