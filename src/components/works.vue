<template>
  <default-section title="works">
    <v-row>
      <v-col md="6" v-for="(i, k) in 4" :key="k">
        <work-card></work-card>
      </v-col>
    </v-row>
    <p class="text-center mt-10">
      <v-btn outlined rounded color="primary" large>more works</v-btn>
    </p>
  </default-section>
</template>
<script>
import defaultSection from "./layout/defaultSection.vue";
import workCard from "./single/workCard.vue";
export default {
  components: {
    defaultSection,
    workCard,
  },
};
</script>
