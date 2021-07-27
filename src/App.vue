<template>
  <v-app>
    <v-app-bar app color="primary" elevate-on-scroll dark height="70">
      <v-container
        fluid
        class="d-flex justify-space-between"
        style="width: 100%"
      >
        <div
          class="d-flex align-center text-capitalize text-h4 font-weight-black"
        >
          <router-link to="/" class="white--text" style="text-decoration: none">
            misicod .
          </router-link>
        </div>

        <div class="d-none d-md-inline-flex">
          <v-btn @click="$vuetify.goTo('#hero')" text to="/"> home </v-btn>
          <span v-if="$route.name == 'Home'">
            <v-btn text @click="$vuetify.goTo('#about')"> about </v-btn>
            <v-btn text @click="$vuetify.goTo('#experties')"> experties </v-btn>
            <v-btn text @click="$vuetify.goTo('#testimonial')">
              testimonials
            </v-btn>
          </span>
          <span>
            <v-btn text to="/works">works</v-btn>
            <v-btn text to="/contact"> contacts</v-btn>
          </span>
        </div>
        <v-app-bar-nav-icon
          class="d-md-none"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </v-container>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app temporary clipped-left>
      <div class="primary px-3 py-6">
        <p class="font-weight-black white--text text-h5 text-capitalize">
          misicod
        </p>
      </div>
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="primary--text ">
          <v-list-item
            v-for="(routerLink, i) in routerLinks"
            :key="i"
            :to="routerLink.link"
          >
            <v-list-item-title class="text-capitalize">
              {{ routerLink.name }}
            </v-list-item-title>
          </v-list-item>
          <span v-if="$route.name == 'Home'">
            <v-list-item @click="$vuetify.goTo('#about')">
              <v-list-item-title class="text-capitalize">
                about
              </v-list-item-title>
            </v-list-item>
            <v-list-item @click="$vuetify.goTo('#experties')">
              <v-list-item-title class="text-capitalize">
                experties
              </v-list-item-title>
            </v-list-item>
            <v-list-item @click="$vuetify.goTo('#testimonial')">
              <v-list-item-title class="text-capitalize">
                testimonials
              </v-list-item-title>
            </v-list-item>
          </span>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view />
    </v-main>

    <v-footer color="black" dark>
      <v-container>
        <v-row no-gutters>
          <v-col md="12" class="text-center">
            <p class="text-h4 text-capitalize primary--text font-weight-bold">
              misicod
            </p>
            <v-row justify="center">
              <v-col cols="8">
                <p>
                  I'm a great fan of football, well thats a comment you wouldn't
                  want to hear but, if i told you what you expected, that would
                  make me predictable. Thats something I'm not , I'm a
                  techpreneur, getting societal problems solved is what unwinds
                  my minds.
                </p>
              </v-col>
            </v-row>

            <p>
              <v-btn
                icon
                color="primary"
                v-for="(sociallink, i) in sociallinks"
                :key="i"
                :href="sociallink.link"
              >
                <v-icon>{{ sociallink.icon }}</v-icon>
              </v-btn>
            </p>
          </v-col>
          <!-- <v-col class="py-4 white--text" cols="12">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-col> -->
        </v-row>
        <v-divider></v-divider>
        <br />
        <br />

        <p class="text-capitalize text-center">
          this website is designed and maintained by
          <v-btn color="primary" text class="px-0">chmod</v-btn>
        </p>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    routerLinks: [
      {
        name: "home",
        link: "/",
      },
      {
        name: "works",
        link: "/works",
      },
      {
        name: "contact",
        link: "/contact",
      },
    ],
    drawer: false,
    group: null,
    sociallinks: [
      {
        icon: "mdi-linkedin",
        link: "",
      },
      {
        icon: "mdi-instagram",
        link: "",
      },
      {
        icon: "mdi-pinterest",
        link: "",
      },
      {
        icon: "mdi-github",
        link: "",
      },
    ],
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
        title: "experties",
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
