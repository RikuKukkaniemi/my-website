<template>
  <div>
    <p class="text-center text-h4 my-3">Esittely</p>
    <HeaderUnderliner />
    <v-card
      elevation="0"
      color="transparent"
      class="text-center mx-auto"
      width="900px"
    >
      <v-card-subtitle class="pb-10"
        ><v-avatar size="200">
          <img src="../assets/face.png" alt="my picture" /> </v-avatar
      ></v-card-subtitle>
      <v-card-text class="px-14">
        <div class="text--primary body-1">
          Olen työskennellyt sovelluskehityksen parissa vuodesta 2018 lähtien. Tällä hetkellä koen olevani vahvimmilla backend painotteisessa kehityksessä ja suunnittelussa. Kokemusta löytyy myös frontend kehityksestä moderneilla JavaScript-sovelluskehyksillä.
        </div>
        <div class="text--primary mt-4 body-1">
          Tykkään panostaa koodissa laatuun ja muokattavuuteen. Olen tottunut hallinnoimaan laatua esimerkiksi koodikatselmoinneilla, yksikkötesteillä ja CI/CD-käytänteillä. Koodin laatuun ja muokattavuuteen pystyy mielestäni parhaiten vaikuttamaan jo suunnitteluvaiheessa.
          Tästä syystä ominaisuuksien prototypointi ja UML-kaavioiden laatiminen on järkevää. Mielestäni suunnittelussa on myös tärkeää ottaa huomioon koodin muokattavuus, minkä vuoksi olen tottunut noudattamaan sovelluskehityksessä <a
            href="https://en.wikipedia.org/wiki/SOLID"
            class="text-decoration-none"
            >SOLID</a
          >-arkkitehtuuriperiaatteita.
        </div>         
          
        <div class="text--primary mt-4 body-1">
          Olen suorittanut tietotekniikan maisterikoulutuksen Jyväskylän
          yliopistossa. Alan koulutus ei kuitenkaan ole jäänyt siihen, sillä
          olen itseopiskellut useita erilaisia kursseja
          <a href="https://www.udemy.com/" class="text-decoration-none">Udemy</a
          >-sivustolla. Arvostan työnantajaa, joka antaa käyttää työaikaa uuden opiskeluun.
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
