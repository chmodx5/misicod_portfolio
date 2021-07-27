<template>
  <div>
    <v-parallax light height="500" src="@/assets/hero.svg">
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
            <p class="text-h3 font-weight-black primary--text">
              my name is emmanuel
            </p>
            <p class="text-h2 font-weight-black">mechatronics engineer</p>
            <p class="text-capitalize">
              finalist mechatrionics engineering student and hardworking
              individual who loves football
            </p>
            <p><v-btn to="/contact" large> contact me</v-btn></p>
          </v-container>
        </div>
      </v-overlay>
    </v-parallax>
  </div>
</template>
