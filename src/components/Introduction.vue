<template>
  <v-card shaped max-width="700" class="mx-auto text-center">
    <v-card-subtitle class="headline text--primary pb-0">Moi, nimeni on Riku. </v-card-subtitle>
    <v-card-subtitle class="title text--primary pt-0">Olen sovelluskehittäjä.</v-card-subtitle>
    <v-card-text>
      <div
        class="text--primary"
      >Minulla on työkokemusta ohjelmoinnista {{ getExperienceYears }} vuotta, {{ getExperienceMonths }} kuukautta ja {{ getExperienceDays }} päivää.</div>
      <div class="text--primary">Koulutukseltani olen filosofian maisteri pääaineena tietotekniikka.</div>
      <ContactDetails class="mt-3" />
    </v-card-text>
  </v-card>
</template>

<script>
import moment from "moment";
import ContactDetails from "./ContactDetails";

export default {
  components: {
    ContactDetails,
  },
  methods: {
    getExperienceDate: function (year = "2018", month = "01", day = "15") {
      return moment(`${year}-${month}-${day}`, "YYYY-MM-DD");
    },
  },
  computed: {
    getExperienceYears: function () {
      return moment().diff(this.getExperienceDate(), "years");
    },
    getExperienceMonths: function () {
      return moment().diff(
        this.getExperienceDate(moment().format("YYYY")),
        "months"
      );
    },
    getExperienceDays: function () {
      return moment().diff(
        this.getExperienceDate(moment().format("YYYY"), moment().format("M")),
        "days"
      );
    },
  },
};
</script>