<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="8">
      <v-card class="page-wrapper">
        <ul class="post-list">
          <li v-for="post in posts" :key="post.id">
            <NuxtLink :to="`blog/${post.slug}`">{{
              post.title.charAt(0).toUpperCase() + post.title.slice(1)
            }}</NuxtLink>
          </li>
        </ul>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  async asyncData() {
    const posts = await fetch(
      'https://jamstack-backend.herokuapp.com/posts'
    ).then((res) => res.json())
    return { posts }
  },
}
</script>

<style lang="scss">
.page-wrapper {
  padding: 20px;
}
.post-list {
  list-style: none;
  padding: 0 !important;
  li a {
    color: #fff;
  }
}
</style>
