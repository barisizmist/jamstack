<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8">
      <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
        <JamstackLogo />
      </v-card>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js Jamstack template
        </v-card-title>
        <v-card-text>
          <p>
            Nuxt an open source vue framework making web development simple and
            powerful.
          </p>
          <a
            href="https://nuxtjs.org/"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt Documentation
          </a>
          <hr class="my-3" />
          <p>
            The modern way to build Websites and Apps that delivers better
            performance
          </p>
          <a
            href="https://jamstack.org/"
            target="_blank"
            rel="noopener noreferrer"
          >
            Jamstack Documentation
          </a>
          <hr class="my-3" />
          <p>
            Vuetify is a progressive Material Design component framework for
            Vue.js. It was designed to empower developers to create amazing
            applications.
          </p>
          <a
            href="https://vuetifyjs.com"
            target="_blank"
            rel="noopener noreferrer"
          >
            Vuetify documentation
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/blog"> Blog </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>
<style scoped>
img,
svg {
  margin: 5px;
}
.logo {
  flex-wrap: wrap;
}
</style>
