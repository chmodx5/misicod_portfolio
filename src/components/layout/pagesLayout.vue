<template>
  <div>
    <div>
      <v-parallax light height="300" src="@/assets/hero.svg">
        <v-overlay
          absolute
          color="white"
          opacity="0.9"
          class="d-flex justify-start"
          light
        >
          <div
            class="text-uppercase font-weight-black black--text"
            style="width: 100vw !important"
          >
            <v-container>
              <p class="text-h2 font-weight-black">{{ $route.name }}</p>

              <p>
                <v-btn large left to="/">
                  <v-icon class="mr-3">mdi-arrow-left</v-icon> back</v-btn
                >
              </p>
            </v-container>
          </div>
        </v-overlay>
      </v-parallax>
    </div>
    <default-section>
      <slot />
    </default-section>
  </div>
</template>
<script>
import defaultSection from "@/components/layout/defaultSection.vue";
export default {
  components: {
    defaultSection,
  },
};
</script>
