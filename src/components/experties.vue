<template>
  <default-section title="my experties">
    <v-row>
      <v-col cols="12" md="6" v-for="(i, k) in 4" :key="k">
        <experties-card
          icon="mdi-domain"
          title="exterpise design"
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus ipsa temporibus distinctio minima beatae, vel impedit voluptatum illum sunt laborum facere aperiam accusamus maxime esse modi a numquam corporis suscipit?"
          linktitle="something"
          link="/"
        />
      </v-col>
    </v-row>
  </default-section>
</template>
<script>
import defaultSection from "./layout/defaultSection.vue";
import expertiesCard from "./single/expertiesCard.vue";
export default {
  components: {
    defaultSection,
    expertiesCard,
  },
};
</script>
