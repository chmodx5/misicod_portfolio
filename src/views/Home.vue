<template>
  <div>
    <hero />
    <experties />
    <works />
    <about />
    <testimonial />
  </div>
</template>

<script>
import experties from "../components/experties";
import works from "../components/works";
import about from "../components/about";
import testimonial from "../components/testimonial";
import hero from "../components/hero.vue";

export default {
  name: "Home",

  components: {
    experties,
    works,
    about,
    testimonial,
    hero,
  },
};
</script>
