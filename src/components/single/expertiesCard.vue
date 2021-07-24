<template>
  <v-card rounded="lg" hover outlined class="pa-6">
    <v-icon size="50" color="gray lighten-4"> {{ icon }} </v-icon>
    <br />
    <p class="text-capitalize font-weight-bold text-h5 mt-6">
      {{ title }}
    </p>
    <p>
      {{ text }}
    </p>
    <v-btn :to="link" text color="primary">{{ linktitle }}</v-btn>
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
