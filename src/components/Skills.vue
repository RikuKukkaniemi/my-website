<template>
  <div>
    <h2 class="text-center my-3">Osaaminen</h2>
  
  <v-card
    class="mx-auto"
    max-width="300"
  >
    <v-list flat>
      <v-subheader>Backend</v-subheader>
      <v-list-item-group>
        <v-list-item
          v-for="(language, l) in backend"
          :key="l"
        >
          <v-list-item-icon>
            <v-icon :color="language.icon.color" v-text="language.icon.code"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="language.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <v-divider />
    <v-list flat>
    <v-subheader>Frontend</v-subheader>
    <v-list-item-group>
        <v-list-item
          v-for="(language, l) in frontend"
          :key="l"
        >
          <v-list-item-icon>
            <v-icon :color="language.icon.color" v-text="language.icon.code"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="language.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
      backend: [
        {
          icon: {
            color: 'red',
            code: 'mdi-laravel',
          },
          text: 'Laravel'
        },
        {
          icon: {
            color: 'blue',
            code: 'mdi-language-php',
          },
          text: 'PHP'
        },
        {
          icon: {
            color: 'blue',
            code: 'mdi-language-python',
          },
          text: 'Python'
        },
      ],
      frontend: [
        {
          icon: {
            color: 'green',
            code: 'mdi-vuejs',
          },
          text: 'Vue.js'
        },
        {
          icon: {
            color: 'yellow',
            code: 'mdi-language-javascript',
          },
          text: 'JavaScript'
        },
        {
          icon: {
            color: 'blue',
            code: 'mdi-vuetify',
          },
          text: 'Vuetify'
        },
      ]
    }),
}
</script>