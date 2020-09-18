<template>
  <div class="content">
    <b-container>
      <h1>{{ post.title }}</h1>
      <p class="font-weight-bold">Published Date: <time :datetime="post.date">{{ formatDate }}</time></p>
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
  },

  computed: {
    formatDate () {
      return new Date(this.post.date).toLocaleDateString()
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
.detail {
  font-size: 18px;
  line-height: 1.7;

  /deep/ p {
    font-size: 18px;
    line-height: 1.7;
  }

  img,
  iframe,
  video {
    max-width: 100%;
    max-height: 400px;
    overflow: hidden;
  }
}

img {
  max-width: 100%;
}
</style>
