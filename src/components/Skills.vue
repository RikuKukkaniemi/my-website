<template>
  <div>
    <h2 class="text-center my-3">Osaaminen</h2>
    <v-card class="mx-auto" max-width="344">
      <v-treeview dense open-all :items="items"></v-treeview>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        id: 1,
        name: "Backend :",
        children: [
          { id: 2, name: "Laravel" },
          { id: 3, name: "PHP" },
        ]
      },
    ]
  })
};
</script>