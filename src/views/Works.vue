<template>
  <pages-layout>
    <v-row>
      <v-col class="d-flex" md="6" v-for="(work, k) in works" :key="k">
        <work-card
          class="flex-grow-1"
          :desc="work.desc"
          :image="work.image"
          :title="work.title"
          :link="work.link"
        ></work-card>
      </v-col>
    </v-row>
  </pages-layout>
</template>
<script>
import pagesLayout from "@/components/layout/pagesLayout.vue";
import workCard from "@/components//single/workCard.vue";
export default {
  data: () => ({
    works: [
      {
        image: "touchless_faucet.jpg",
        title: "touchless faucet with door control system for covid",
        desc: "As someone approaches an entrance with this mechanism,there is a “Please wash your hands” message displayed by the LCD. Once the person moves closer to the faucet, the ultrasonic sensor, sensing proximity, sends a signal to the servo motor which in turn rotates the pump.",
        link: "https://github.com/YvonneMureithi/Touchless-Faucet",
      },
      {
        image: "face_and_mask_atm.jpg",
        title: "face mask ATM and reminder",
        desc: "The project is a proof of concept of a mask dispensing ATM that can be installed at homes to remind people to take a mask before leaving or at the entrance of public facilities. When someone comes into close proximity with the dispenser, a buzzer goes off and a text reminding one to pick a mask is displayed. ",
        link: "https://github.com/r3wnad/Mask-ATM",
      },
      {
        image: "simple_pulse_monitor.jpg",
        title: "simple pulse monitor",
        desc: "The pulse sensor module has a light that helps in measuring the pulse rate. When we place the finger on the pulse sensor, the light reflected will change based on the volume of blood inside the capillary blood vessels.",
      },
      {
        image: "stepper_control.jpg",
        title: "stepper motor control using BLYK app",
        desc: "Blynk is a platform that allows you to quickly build interfaces for controlling and monitoring your hardware projects from your iOS and Android device. After downloading the Blynk app, you can create a project dashboard and arrange buttons, sliders, graphs, and other widgets onto the screen. ",
        link: "https://github.com/MisiCod/Stepper-control-from-the-phone",
      },
      {
        image: "voice_control.jpg",
        title: "voice controlled home appliances",
        desc: "This is a project which is supposed to enable one to control home appliances by use of voice commands communicated to the Google Assistant, which then prompts the desired actions. In this case, we used voice commands to turn an LED on or/ and off.  ",
        link: "https://github.com/MisiCod/Stepper-control-from-the-phone",
      },
      {
        image: "automated_door.jpg",
        title: "automated door system",
        desc: "This project involves coming up with a proof-of-concept automatic door system that helps reduce coming into contact with contaminated surfaces, an example is, a door in a public place , most especially during this day and age of Covid-19.",
        link: "https://github.com/wambui-pixel/Automatic-Door",
      },
      {
        image: "smoke_detector.jpg",
        title: "automated smoke detector",
        desc: "This smoke detector project is a proof of concept that you can be able to capture and send data to the cloud from NodeMCU using the Blynk App. It detects smoke beyond a set threshold and sends a notification to the Blynk App",
        link: "https://github.com/wambui-pixel/Smoke-detector",
      },
    ],
  }),
  components: {
    pagesLayout,
    workCard,
  },
};
</script>
