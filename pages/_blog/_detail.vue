<template>
  <div class="content">
    <b-container>
      <h1>{{ post.title }}</h1>
      <div v-if="post.large_image">
        <img :src="post.large_image" class="img-fluid rounded">
      </div>
      <div v-html="post.body" class="mt-4 detail" />
    </b-container>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params, error }) {
    let post
    try {
      post = await $content('blog', params.detail).fetch()
    } catch (e) {
      error({ message: 'Blog Post not found' })
    }

    return {
      post
    }
  }
}
</script>
<style lang="scss" scoped>
.content {
  padding: 40px 0;
}
h1 {
  color: $secondary;
  margin-bottom: 20px;
  font-weight: 900;
}
.detail p {
  font-size: 18px;
  line-height: 1.7;
}
</style>
