<template>
  <v-row>
    <v-col class="text-center">
      <div v-for="(p, i) in posts" :key="i">
        <div class="text-center">{{ p.title }}</div>
        {{ p.content }}
      </div>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      posts: [],
    }
  },
  // created() {
  //   this.getPosts()
  // },
  async fetch() {
    this.posts = await fetch('http://localhost:1337/posts').then((res) =>
      res.json()
    )
  },
  // methods: {
  //   getPosts() {
  //     fetch('http://localhost:1337/posts')
  //       .then((res) => res.json())
  //       .then((data) => (this.posts = data))
  //   },
  // },
}
</script>
