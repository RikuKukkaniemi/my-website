<template>
  <div>
    <h2 class="text-center my-3">Työkokemus</h2>
    <v-timeline>
      <v-timeline-item v-for="(job, j) in jobs" :key="j" :color="job.color">
        <template v-slot:opposite>
          <span :class="`headline font-weight-bold ${job.color}--text`" v-text="job.year"></span>
        </template>
        <v-card class="elevation-2">
          <v-card-title class="headline">{{ job.title }}</v-card-title>
          <v-card-text>{{ job.description }}</v-card-text>
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
        year: "01/2019-",
        title: "Paytrail, sovelluskehittäjä",
        description:
          "Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae."
      },
      {
        color: "blue",
        year: "01/2018-12/2018",
        title: "Jyväskylän yliopisto, tutkimusavustaja",
        description:
          "Terveydenhuoltoon liittyvien prototyyppien ohjelmointi. Prototyypeissä pyritty hyödyntämään tekoälyä käyttäen pääosin IBM Watson työkaluja."
      }
    ]
  })
};
</script>