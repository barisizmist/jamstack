<template>
  <div>
    <h2>{{ post.title }}</h2>
    <div>{{ post.body }}</div>
  </div>
</template>

<script>
export default {
  async asyncData({ params }) {
    const post = await fetch(
      `https://jsonplaceholder.typicode.com/posts/${params.id}`
    ).then((res) => res.json())
    return { post }
  },
}
</script>

<style></style>
