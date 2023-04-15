<template>
  <v-container class="fill-height">
    <v-responsive class="d-flex align-center text-center fill-height">
      <h1 class="text-h2 font-weight-bold">Some title</h1>

      <v-row no-gutters class="d-flex align-center justify-center pa-6">
        <Sliders> </Sliders>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script setup>
import Sliders from "./Sliders.vue";
</script>
