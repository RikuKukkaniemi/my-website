<template>
  <div>
    <p class="text-center my-3 text-h4">Experience</p>
    <HeaderUnderliner />
    <v-card elevation="0" color="transparent" class="mx-auto" max-width="1500">
      <v-timeline :dense="$vuetify.breakpoint.smAndDown">
        <v-timeline-item v-for="(job, j) in jobs" :key="j">
          <template v-slot:opposite>
            <span :class="`headline font-weight-bold`" v-text="job.time"></span>
          </template>
          <v-card class="elevation-2 mx-md-4 me-4">
            <v-card-title :class="`headline font-weight-boldt`">{{ job.title }}</v-card-title>
            <v-card-subtitle v-if="$vuetify.breakpoint.smAndDown">{{ job.time }}</v-card-subtitle>
            <v-card-text>
              <p v-for="(paragraph, index) in job.description" :key="index">{{ paragraph }}</p>
              <p v-if="job.link">
                {{ job.link.description }}
                <a :href="job.link.href">{{ job.link.href }}</a>
              </p>
              <div>
                <v-chip v-for="(keyword, index) in job.keywords" :key="index">
                  {{ keyword }}
                </v-chip>
              </div>
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
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
    jobs: [
      {
        time: "01/2019 - 09/2021",
        title: "Software Developer, Paytrail",
        description: [
          "Mostly backend development and desiging in a team of 4.",
        ],
        keywords: ['PHP/Laravel', 'Docker', 'PHPUnit', 'MySQL', 'Microservices', 'UML', 'CI/CD', 'Vue.js', 'Jira', 'Kanban', 'SOLID']
      },
      {
        time: "01/2018 - 12/2018",
        title: "Research Programmer, Jyväskylän yliopisto",
        description: [
          "Työskentelin projektissa, jossa selvitettiin, miten tekoälyä voitaisiin hyödyntää terveydenhuollossa. Työnkuvaan kuului tekoälyprototyyppien suunnittelua ja ohjelmointia 3-5 hengen tiimeissä.",
          'Projektin tuloksista kirjoitettiin tieteellinen julkaisu "Tekoälypohjaisten teknologioiden testaus prototyyppisovelluksilla". Julkaisussa kerrotaan projektissa käytetyistä tekoälyteknologoista ja esitellään toteutettuja prototyyppejä.',
        ],
        keywords: ['PHP/Laravel', 'Docker', 'PHPUnit', 'MySQL', 'Microservices', 'UML', 'CI/CD', 'Vue.js', 'Jira', 'Kanban', 'SOLID'],
        link: {
          description: "Linkki julkaisuun: ",
          href: "https://jyx.jyu.fi/handle/123456789/63938",
        },
      },
    ],
  }),
};
</script>