<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <b-container>
        <h1 class="font-weight-bold">
          Blog
        </h1>
      </b-container>
    </div>
    <div class="blog-list">
      <b-container>
        <b-row>
          <b-col v-for="(post,index) in posts" :key="index" md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" :src="post.thumbnail" alt="Nuts & Dried fruits">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  {{ post.title }}
                </h5>
                <p class="card-text">
                   {{ post.description }}
                </p>
                <nuxt-link :to="{ name: 'blog-detail', params: { detail: post.slug }}" class="btn btn-secondary">View</nuxt-link>
              </div>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const posts = await $content('blog').fetch()

    return {
      posts
    }
  }
}
</script>

<style lang="scss" scoped>
.jumbotron {
  color: white;
  background-color: $primary;
  background-image: linear-gradient(rgba(0, 0, 0, 0.65) 0%, rgba(0, 0, 0, 0.65) 100%), url('/img/bg1.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0 auto;
  padding: 89px 0 70px;

  @include media-breakpoint-up(lg) {
    padding: 120px 0 90px;
    background-attachment: fixed;
  }
  h1 {
    @include media-breakpoint-up(lg) {
      font-size: 60px;
    }
  }
  p {
    font-size: 22px;
    @include media-breakpoint-up(lg) {
      font-size: 25px;
    }
  }
}

.blog-list {
  padding: 70px 0;
}

.card {
  height: 100%;
}
</style>
