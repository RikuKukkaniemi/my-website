<template>
  <div>
    <h2 class="text-center my-3">Esittely</h2>
    <HeaderUnderliner />
    <v-card
      elevation="0"
      color="transparent"
      class="text-center mx-auto"
      max-width="700"
    >
      <v-card-subtitle class="headline text--primary py-0"
        >Moi, nimeni on Riku.</v-card-subtitle
      >
      <v-card-subtitle class="title text--primary pt-1"
        >Olen sovelluskehittäjä.</v-card-subtitle
      >
      <v-avatar class="mt-2" size="128">
        <img src="../assets/profile.jpg" alt="Riku" />
      </v-avatar>
      <v-card-text>
        <div class="text--primary body-1">
          Olen työskennellut sovelluskehittäjänä vuoden 2018 tammikuusta lähtien. Työnteko
          on ollut enimmäkseen backend painotteista sovelluskehitystä ja
          -suunnittelua. Sovelluskehityksessä olen oppinut noudattamaan
          <a
            href="https://en.wikipedia.org/wiki/SOLID"
            class="text-decoration-none"
            >SOLID</a
          >-arkkitehtuuriperiaatteita.
        </div>
        <div class="text--primary mt-4 body-1">
          Olen suorittanut tietotekniikan maisterikoulutuksen Jyväskylän
          yliopistossa. Alan koulutus ei kuitenkaan ole jäänyt siihen, sillä
          olen itseopiskellut useita eri kursseja
          <a href="https://www.udemy.com/" class="text-decoration-none">Udemy</a
          >-sivustolla.
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
import HeaderUnderliner from "./utility/HeaderUnderliner";

export default {
  components: {
    HeaderUnderliner,
  },
};
</script>
