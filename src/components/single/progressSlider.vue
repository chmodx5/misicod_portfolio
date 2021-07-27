<template>
  <div class="mb-6">
    <div class="d-flex justify-space-between text-h6 text-capitalize">
      <span class="font-weight-bold">{{ title }}</span>
      <span class="primary--text">{{ percentage }}%</span>
    </div>
    <v-progress-linear
      rounded
      height="8"
      :value="percentage"
    ></v-progress-linear>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    percentage: String,
  },
};
</script>
