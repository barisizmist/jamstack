<template>
  <v-row>
    <v-col class="text-center">
      <div v-for="(p, i) in posts" :key="i">
        <div>{{ p.title }}</div>
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
  created() {
    this.getPosts()
  },
  methods: {
    getPosts() {
      fetch('http://localhost:1337/posts')
        .then((res) => res.json())
        .then((data) => (this.posts = data))
    },
  },
}
</script>
