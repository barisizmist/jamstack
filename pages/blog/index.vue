<template>
  <div>
    <h1>Posts</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <NuxtLink :to="`blog/${post.id}`">{{ post.title }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const posts = await fetch('http://localhost:1337/posts').then((res) =>
      res.json()
    )
    return { posts }
  },
}
</script>

<style lang="scss" scoped></style>
