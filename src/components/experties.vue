<template>
  <default-section title="my expertise">
    <v-row>
      <v-col
        class="d-flex"
        cols="12"
        md="6"
        v-for="(experty, k) in experties"
        :key="k"
      >
        <experties-card
          class="flex-grow-1"
          :icon="experty.icon"
          :title="experty.title"
          :text="experty.text"
          :linktitle="experty.linktitle"
          :link="experty.link"
        />
      </v-col>
    </v-row>
  </default-section>
</template>
<script>
import defaultSection from "./layout/defaultSection.vue";
import expertiesCard from "./single/expertiesCard.vue";
export default {
  data: () => ({
    experties: [
      {
        icon: "mdi-printer-3d",
        title: "coreldraw & CAD ",
        text: "I work with both inventor on technical Cad drawings and Corel draw for both descriptive drawings and flow charts",
        linktitle: "learn more",
        link: "https://en.wikipedia.org/wiki/Computer-aided_design",
      },
      {
        icon: "mdi-chip",
        title: "microController programming",
        text: "Involves programing from , arduino, raspberrypi to Atmel AVR's. This includes automation with different sensors, actuation devices and platforms like IoT",
        linktitle: "learn more",
        link: "https://en.wikipedia.org/wiki/Microcontroller",
      },
      {
        icon: "mdi-pencil-ruler",
        title: "electro-mechanical design",
        text: "Working with different circuitrys with an intent to give a desired logic to a system.This reduces cyber attacks",
        linktitle: "learn more",
        link: "https://en.wikipedia.org/wiki/Category:Electromechanical_engineering#:~:text=Electromechanical%20engineering%20(alternatively%20written%20as,electronic%20circuits%20and%20mechanical%20systems.",
      },
      {
        icon: "mdi-web",
        title: "web design",
        text: "nvolves webdevelopment, both back and front end programming of websites and boostrap templates for various desired works.",
        linktitle: "learn more",
        link: "https://en.wikipedia.org/wiki/Web_design",
      },
    ],
  }),
  components: {
    defaultSection,
    expertiesCard,
  },
};
</script>
