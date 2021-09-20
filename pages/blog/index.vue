<template>
  <div>
    <h1>Posts {{ count }}</h1>
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
    const posts = await fetch(
      'https://jsonplaceholder.typicode.com/posts'
    ).then((res) => res.json())
    const count = posts.length
    return { posts, count }
  },
  data() {
    return {
      count: 0,
    }
  },
}
</script>

<style lang="scss" scoped></style>
