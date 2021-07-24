<template>
  <div class="py-10">
    <v-container>
      <p class="text-h3 text-capitalize font-weight-bold mb-12">{{ title }}</p>
      <slot />
    </v-container>
  </div>
</template>
<script>
export default {
  name: "defaultSection",
  props: {
    title: String,
  },
};
</script>
