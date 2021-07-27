<template>
  <div>
    <hero id="hero" />
    <experties id="experties" />
    <works id="works" />
    <about id="about" />
    <testimonial class="text-center" id="testimonial" />
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
