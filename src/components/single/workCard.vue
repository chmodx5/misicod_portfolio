<template>
  <v-card outlined hover rounded="lg">
    <v-img
      :src="require(`@/assets/work/${image}`)"
      :aspect-ratio="16 / 9"
    ></v-img>

    <v-card-title class="text-capitalize mb-4"> {{ title }} </v-card-title>

    <v-card-subtitle>
      <p>
        {{ desc }}
        <span
          ><v-btn
            :href="link"
            target="_blank"
            text
            color="primary"
            class="pa-0 ma-0"
            >more</v-btn
          ></span
        >
      </p>
    </v-card-subtitle>
  </v-card>
</template>

<script>
export default {
  name: "workCard",
  props: {
    image: String,
    title: String,
    desc: String,
    link: String,
  },
};
</script>
