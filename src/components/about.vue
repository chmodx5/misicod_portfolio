<template>
  <default-section title="about">
    <v-row>
      <v-col md="6">
        <div>
          <p>
            I'm a great fan of football, well thats a comment you wouldn't want
            to hear but, if i told you what you expected, that would make me
            predictable. Thats something I'm not , I'm a techpreneur, getting
            societal problems solved is what unwinds my minds.
          </p>
          <p>
            This I do by offering tech-automated solutions ,I've a hands on
            experience in mechanical, electrical, programming and technical
            drawing fields. Whose prowess I have showcased on different
            platforms as put on the gallery.
          </p>
          <p class="primary--text font-weight-bold text-h6">
            " The longer you stare at two dots the more you see the connection "
          </p>
        </div>
      </v-col>
      <v-col>
        <progress-slider title="markup" percentage="50"></progress-slider>
        <progress-slider
          title="user experience design"
          percentage="38"
        ></progress-slider>
        <progress-slider
          title="backend design"
          percentage="98"
        ></progress-slider>
      </v-col>
    </v-row>
  </default-section>
</template>
<script>
import defaultSection from "./layout/defaultSection.vue";
import progressSlider from "./single/progressSlider.vue";
export default {
  components: {
    defaultSection,
    progressSlider,
  },
};
</script>
