<template>
  <div>
    <h2 class="text-center my-3">Esittely</h2>
    <HeaderUnderliner />
    <v-card elevation="0" color="transparent" class="text-center mx-auto" max-width="700">
      <v-card-subtitle class="headline text--primary py-0">Moi, nimeni on Riku.</v-card-subtitle>
      <v-card-subtitle class="title text--primary pt-1">Olen full-stack -kehittäjä.</v-card-subtitle>
      <v-card-text>
        <div class="text--primary body-1">
          Olen työskennellut sovelluskehittäjänä vuodesta 2018 lähtien. Työskentely on ollut enimmäkseen backend painotteista sovelluskehitystä ja -suunnittelua, mutta mukaan on kuulunut jonkin verran myös frontend kehitystä. Sovelluskehityksessä olen tottunut toteuttamaan
          <a
            href="https://en.wikipedia.org/wiki/SOLID"
            class="text-decoration-none"
          >SOLID</a>-arkkitehtuuriperiaatteita. Minulta löytyy myös kiitettävällä arvosanalla suoritettu maisterin tutkinto, jossa opiskelin pääaineena tietotekniikkaa.
        </div>
        <div
          class="text--primary mt-4 body-1"
        >Vaikka työnpuolesta tuleekin tuijotettua paljon tietokoneen ruutua, viihdyn silti suurimman osan vapaa-ajastani tietokoneen äärellä. Pyrin kuitenkin harrastuksillani hakemaan tasapainoa tietokoneen äärellä istumiseen. Harrastuksiini kuuluu tietokoneella pelaaminen, kehonpainoharjoittelu, lentopallo ja frisbeegolf. Vapaa-ajalla tulee satunnaisesti harrastettua myös koodausta. Vapaa-ajan koodauksessa pyrin kokeilemaan minulle uusia ohjelmointikieliä tai -teknologioita, jotta ammatillinen kehittymiseni pysyy ajantasalla myös siltä osin, mitä työpaikalla ei tule tehtyä.</div>
      </v-card-text>
      <v-avatar class="mt-2" size="128">
        <img src="../assets/profile.jpg" alt="Riku" />
      </v-avatar>
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
