<template>
  <default-section title="client testimonial">
    <template>
      <v-carousel
        height="auto"
        :show-arrows="false"
        hide-delimiter-background
        light
        cycle
      >
        <v-carousel-item v-for="(testimonial, i) in testimonials" :key="i">
          <div class="mb-16">
            <img
              height="100"
              width="100"
              :aspect-ratio="1 / 1"
              :src="testimonial.image"
              alt="John"
              style="border-radius: 50%"
            />

            <p class="text-h5 font-weight-bold text-capitalize mt-6">
              {{ testimonial.name }}
            </p>
            <p class="mt-3 text-capitalize primary--text">
              {{ testimonial.position }}
            </p>
            <v-row justify="center">
              <v-col cols="12" md="8">
                <p>
                  {{ testimonial.testimonial }}
                </p>
              </v-col>
            </v-row>

            <p>
              <span class="mr-3"><v-icon size>mdi-phone</v-icon></span
              >: <span class="ml-3">{{ testimonial.phone }}</span>
            </p>
            <p>
              <span class="mr-3"><v-icon size>mdi-at</v-icon></span
              >: <span class="ml-3">{{ testimonial.email }}</span>
            </p>
          </div>
        </v-carousel-item>
      </v-carousel>
    </template>
  </default-section>
</template>
<script>
import defaultSection from "./layout/defaultSection.vue";
export default {
  data: () => ({
    testimonials: [
      {
        image: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
        name: "ngugi",
        position: "general overseer of gearbox",
        testimonial:
          " He has met or surpassed his goals and takes pride in his performance; he is open to ideas and enthusiastic about the opportunity to learn new skills",
        phone: "0712345678",
        email: "ngugi@gmail.com",
      },
      {
        image: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
        name: "limo patrick",
        position: "rearbox professional",
        testimonial:
          " He is consistently willing to view problems as challenges, as opposed to roadblocks and work with others on solutions; he has exhibited an ability to come up with innovative solutions to unexpected problems.",
        phone: "+254 710504790",
        email: "limopato254@gmail.com",
      },
      {
        image: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
        name: "alex muchiri",
        position: "aeronautical engineer",
        testimonial:
          "He has met or surpassed his goals and takes pride in his performance; he is open to ideas and enthusiastic about the opportunity to learn new skills",
        phone: "+254 710504790",
        email: "alexmuchiri11@gmail.com",
      },
    ],
  }),
  components: {
    defaultSection,
  },
};
</script>
