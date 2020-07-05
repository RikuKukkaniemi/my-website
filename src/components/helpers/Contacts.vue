<template>
  <div>
    <v-btn
      v-for="(contact, c) in contacts"
      :key="c"
      class="mx-4 white--text"
      icon
      :href="contact.href"
    >
      <v-icon size="24px">{{ contact.icon }}</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  data: () => ({
    contacts: [
      {
        icon: "mdi-github",
        href: "https://github.com/RikuKukkaniemi"
      },
      {
        icon: "mdi-linkedin",
        href: "https://www.linkedin.com/in/riku-kukkaniemi-7a3942167/"
      }
    ]
  })
};
</script>