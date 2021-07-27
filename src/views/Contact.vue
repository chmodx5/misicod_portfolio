<template>
  <pages-layout>
    <default-section title="get in touch">
      <v-row>
        <v-col md="8">
          <v-form v-model="valid">
            <v-row>
              <v-col md="6">
                <v-text-field
                  outlined
                  v-model="name"
                  :rules="nameRules"
                  :counter="25"
                  label="name"
                  required
                ></v-text-field>
              </v-col>
              <v-col md="6">
                <v-text-field
                  outlined
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  outlined
                  v-model="subject"
                  :rules="subjectRules"
                  :counter="50"
                  label="Subject"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-textarea
                  v-model="mail"
                  outlined
                  name="input-7-1"
                  label="Enter Your Text"
                  auto-grow
                ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-btn
                  class="mr-4"
                  color="primary"
                  large
                  type="submit"
                  :disabled="!valid"
                >
                  submit
                </v-btn>
              </v-col>
            </v-row>
          </v-form>
        </v-col>
        <v-col md="4">
          <div
            class="d-flex align-center mb-3"
            v-for="(contact, k) in contacts"
            :key="k"
          >
            <div class="mr-6">
              <v-icon x-large> {{ contact.icon }} </v-icon>
            </div>
            <div class="text-capitalize">
              <p class="ma-0 font-weight-bold">{{ contact.title }}</p>
              <p class="ma-0">{{ contact.desc }}</p>
            </div>
          </div>
        </v-col>
      </v-row>
    </default-section>
  </pages-layout>
</template>

<script>
import pagesLayout from "@/components/layout/pagesLayout.vue";
import defaultSection from "@/components/layout/defaultSection";
export default {
  data: () => ({
    contacts: [
      {
        name: "location",
        icon: "mdi-google-maps",
        title: "juja, kiambu",
        desc: "some building",
      },
      {
        name: "phone",
        icon: "mdi-phone",
        title: "+254790467583",
        desc: "mon to fri 8am to 5pm",
      },
      {
        name: "email",
        icon: "mdi-at",
        title: "misicod@gmail.com",
        desc: "send me you querry anytime",
      },
    ],
    valid: false,
    name: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 25 || "Name must be less than 25 characters",
    ],
    subject: "",
    subjectRules: [
      (v) => !!v || "subject is required",
      (v) => v.length <= 50 || "subject must be less than 50 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+/.test(v) || "E-mail must be valid",
    ],
    mail: "",
  }),
  components: {
    pagesLayout,
    defaultSection,
  },
};
</script>
