<template>
  <div>
    <p class="text-center my-3 text-h4">Koulutus</p>
    <HeaderUnderliner />
    <v-card elevation="0" color="transparent" class="mx-auto px-3" max-width="800">
      <v-expansion-panels multiple inset>
        <v-expansion-panel v-for="(education, e) in educations" :key="e">
          <v-expansion-panel-header>{{ education.title }}</v-expansion-panel-header>
          <v-expansion-panel-content>
            <p v-for="(paragraph, p) in education.description" :key="p">{{ paragraph }}</p>
            <p v-if="education.link">
              {{ education.link.description }}
              <a
                :href="education.link.href"
              >{{ education.link.href }}</a>
            </p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
  </div>
</template>

<script>
import HeaderUnderliner from "./utility/HeaderUnderliner";

export default {
  components: {
    HeaderUnderliner,
  },
  data: () => ({
    educations: [
      {
        title: "Filosofian maisteri, Jyväskylän yliopisto",
        description: [
          "2017 – 2020",
          "Pääaineena tietotekniikka ja suuntaavana moduulina ohjelmistotekniikka.",
          "Pro gradu aihe: Luonnollisen suomen kielen ymmärtäminen koneellisesti.",
        ],
        link: {
          description: "Linkki graduun: ",
          href: "https://jyx.jyu.fi/handle/123456789/69035",
        },
      },
      {
        title: "Luonnontieteiden kandidaatti, Jyväskylän yliopisto",
        description: [
          "2014 – 2017",
          "Pääaineena tietotekniikka ja sivuaineina tilastotiede sekä matematiikka.",
          "Kandidaatintutkielman aihe: Miksi pelien virtuaalihyödykkeitä ostetaan?",
        ],
        link: {
          description: "Linkki tutkielmaan: ",
          href: "https://jyx.jyu.fi/handle/123456789/53916",
        },
      },
      {
        title: "Johtajakoulutus, varusmiespalvelus",
        description: ["2011 – 2012", "Ryhmänjohtaja, alikersantti."],
      },
      {
        title: "Ylioppilas, Nurmon lukio",
        description: ["2008 – 2011"],
      },
    ],
  }),
};
</script>