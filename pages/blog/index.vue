<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="8">
      <v-card class="page-wrapper">
        <h2>Posts</h2>
        <ul class="post-list">
          <li v-for="(post, index) in posts" :key="post.id">
            <NuxtLink :to="`blog/${post.slug}`"
              >{{ index + 1 }}-
              {{
                post.title.charAt(0).toUpperCase() + post.title.slice(1)
              }}</NuxtLink
            >
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
  padding: 30px 20px;
}
.post-list {
  list-style: none;
  padding: 0 !important;
  li a {
    color: #fff;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
