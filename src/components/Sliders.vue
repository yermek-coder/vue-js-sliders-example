<template>
  <v-card width="100%" style="margin: auto">
    <v-card-text>
      <v-slider
        v-model="chargebackPerMonth"
        :max="1000000"
        :step="1"
        label="Chargeback per month"
        hide-details
        class="ma-4"
      >
        <template v-slot:append>
          <v-text-field
            v-model="chargebackPerMonth"
            type="number"
            style="width: 150px"
            prefix="#"
            density="compact"
            hide-details
            variant="outlined"
          ></v-text-field>
        </template>
      </v-slider>

      <v-slider
        v-model="averageChargeback"
        :max="10000"
        :step="1"
        label="Average Chargeback Amount"
        hide-details
        class="ma-4"
      >
        <template v-slot:append>
          <v-text-field
            v-model="averageChargeback"
            type="number"
            style="width: 150px"
            prefix="$"
            density="compact"
            hide-details
            variant="outlined"
          ></v-text-field>
        </template>
      </v-slider>

      <v-slider
        v-model="blue"
        :max="100"
        :step="1"
        label="Fee Per Won Chargeback"
        hide-details
        class="ma-4"
      >
        <template v-slot:append>
          <v-text-field
            v-model="blue"
            type="number"
            style="width: 150px"
            density="compact"
            hide-details
            prefix="%"
            variant="outlined"
          ></v-text-field>
        </template>
      </v-slider>

      <div>Added Yearly Revenue Estimate:</div>
      <div>{{ chargebackPerMonth * 12 * averageChargeback * 0.6 * 0.35 }}</div>
    </v-card-text>
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const chargebackPerMonth = ref(0);
const averageChargeback = ref(0);
const blue = ref(0);
</script>
