<template>
  <div>
    <h2 class="text-center my-3">Työkokemus</h2>
    <v-timeline :dense="$vuetify.breakpoint.smAndDown">
      <v-timeline-item v-for="(job, j) in jobs" :key="j" :color="job.color">
        <template v-slot:opposite>
          <span :class="`headline font-weight-bold ${job.color}--text`" v-text="job.time"></span>
        </template>
        <v-card class="elevation-2">
          <v-card-title :class="`headline font-weight-bold ${job.color}--text`">{{ job.title }}</v-card-title>
          <v-card-subtitle v-if="$vuetify.breakpoint.smAndDown">{{ job.time }}</v-card-subtitle>
          <v-card-text>
            <p v-for="(paragraph, p) in job.description" :key="p">
              {{ paragraph }}
            </p>
            <p v-if="job.link">{{ job.link.description }}<a :href="job.link.href">{{ job.link.href }}</a></p>
            </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>

<script>
export default {
  data: () => ({
    jobs: [
      {
        color: "pink",
        time: "01/2019-",
        title: "Paytrail",
        description: [
          "Työskentelyä sovelluskehittäjänä Suomen kattavinta maksupalvelua tarjoavassa yrityksessä. Työnkuvaan kuuluu backend painotteista sovelluskehitystä ja -sunnittelua 4-5 hengen tiimeissä.",
        ],
      },
      {
        color: "blue",
        time: "01/2018-12/2018",
        title: "Jyväskylän yliopisto",
        description: [
          "Työskentelyä tutkimusavustajana projektissa, jossa selvitettiin, miten tekoälyä voitaisiin hyödyntää terveydenhuollossa. Työnkuvaan kuului tekoälyprototyyppien suunnittelua ja ohjelmointia 3-5 hengen tiimeissä.",
          'Projektin tuloksista kirjoitettiin tieteellinen julkaisu "Tekoälypohjaisten teknologioiden testaus prototyyppisovelluksilla". Julkaisussa kerrotaan projektissa käytetyistä tekoälyteknologoista ja esitellään toteutettuja prototyyppejä.',
        ],
        link: {
          description: "Linkki julkaisuun: ",
          href: "https://jyx.jyu.fi/handle/123456789/63938"
        }
      }
    ]
  })
};
</script>