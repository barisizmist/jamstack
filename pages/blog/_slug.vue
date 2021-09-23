<template>
  <v-row justify="center" align="center">
    <v-col class="col-sm-8 col-md-8 col-12">
      <v-card class="page-wrapper">
        <h2>{{ post.title.charAt(0).toUpperCase() + post.title.slice(1) }}</h2>
        <div>{{ post.body.charAt(0).toUpperCase() + post.body.slice(1) }}</div>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  async asyncData({ params }) {
    const post = await fetch(
      `https://jamstack-backend.herokuapp.com/posts/${params.slug}`
    ).then((res) => res.json())
    return { post }
  },
}
</script>

<style lang="scss">
h2 {
  margin-bottom: 20px;
}
</style>
