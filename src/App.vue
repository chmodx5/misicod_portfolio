<template>
  <v-app>
    <v-app-bar app color="primary" elevate-on-scroll dark>
      <v-container
        fluid
        class="d-flex justify-space-between"
        style="width: 100%"
      >
        <div
          class="d-flex align-center text-capitalize text-h5 font-weight-bold"
        >
          <router-link to="/" class="white--text" style="text-decoration: none">
            misicod .
          </router-link>
        </div>

        <div>
          <v-btn text v-for="link in links" :key="link.title" :to="link.link">{{
            link.title
          }}</v-btn>
        </div>

        <div class="d-flex align-center">
          <v-btn outlined rounded> donwload cv </v-btn>
        </div>
      </v-container>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    links: [
      {
        title: "home",
        link: "/",
      },
      {
        title: "about",
        link: "/about",
      },
      {
        title: "service",
        link: "/service",
      },
      {
        title: "contact",
        link: "/contact",
      },
    ],
  }),
};
</script>
