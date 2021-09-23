<template>
  <v-app dark>
    <div class="header-bar">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/blog">Blog</NuxtLink>
    </div>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Blog',
          to: '/blog',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<style lang="scss">
.header-bar {
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #272727;
  a {
    color: #fff !important;
    margin-right: 10px;
    margin-left: 10px;
    text-decoration: none;
  }
}
</style>
