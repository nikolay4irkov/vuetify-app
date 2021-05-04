<template>
  <v-app>
    <v-app-bar dark app color="primary">
      <v-app-bar-title>Vuetify Dashboard</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        rounded
        :to="link.link"
        v-for="link in links"
        :key="`${link.label}-header-link`"
        >{{ link.label }}</v-btn
      >
      <v-btn @click="toggleTheme" text rounded>Toggle theme</v-btn>
    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>

    <v-footer color="primary lighten-1" padless>
      <v-row justify="center" no-gutters>
        <v-btn
          :to="link.link"
          v-for="link in links"
          :key="`${link.label}-footer-link`"
          color="white"
          text
          rounded
          class="my-2"
        >
          {{ link.label }}
        </v-btn>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          label: "Home",
          link: "/",
        },
        {
          label: "Login",
          link: "/login",
        },
        {
          label: "Signup",
          link: "/signup",
        },
        {
          label: "Dashboard",
          link: "/dashboard",
        },
      ],
    };
  },
  methods: {
    toggleTheme() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    },
  },
};
</script>
