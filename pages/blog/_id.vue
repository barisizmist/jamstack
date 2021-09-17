<template>
  <div>
    <h2>{{ post.title }}</h2>
    <div>{{ post.content }}</div>
  </div>
</template>

<script>
export default {
  async asyncData({ params }) {
    const post = await fetch(`http://localhost:1337/posts/${params.id}`).then(
      (res) => res.json()
    )
    return { post }
  },
}
</script>

<style></style>
