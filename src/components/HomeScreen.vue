<template>
  <v-container>
    <v-layout :v-for="event in arrayEvents">
      <span>SASUKEEEEE</span>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    arrayEvents: [0, 1, 2, 3, 4, 5, 6],
  }),
};
</script>
