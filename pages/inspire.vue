<template>
  <v-row>
    <v-col class="text-center">
      <h1>{{ posts.length }}</h1>
    </v-col>
  </v-row>
</template>
<script>
export default {
  async asyncData({ $axios }) {
    const posts = await $axios.$get(
      `https://jsonplaceholder.typicode.com/posts`
    )
    return { posts }
  },
}
</script>
