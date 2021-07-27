<template>
  <v-card rounded="lg" hover outlined class="pa-6">
    <v-icon size="50" color="grey lighten-1"> {{ icon }} </v-icon>
    <br />
    <p class="text-capitalize font-weight-bold text-h5 mt-6">
      {{ title }}
    </p>
    <p>
      {{ text }}
    </p>
    <v-btn :href="link" target="_blank" text color="primary">{{
      linktitle
    }}</v-btn>
  </v-card>
</template>
<script>
export default {
  props: {
    title: String,
    icon: String,
    text: String,
    linktitle: String,
    link: String,
  },
};
</script>
