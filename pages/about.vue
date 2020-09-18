<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <b-container>
        <h1 class="font-weight-bold">
          {{ page.title }}
        </h1>
      </b-container>
    </div>
    <div class="intro">
      <b-container>
        <h2>{{ page.intro }}</h2>
        <p>
          {{ page.intro_content }}
        </p>
      </b-container>
    </div>
    <div class="block">
      <b-container>
        <b-row>
          <b-col v-for="(blk, index) in page.block" :key="index" lg="6" class="mb-4">
            <h4>{{ blk.title }}</h4>
            <div class="content" v-html="$md.render(blk.content)" />
          </b-col>
        </b-row>
      </b-container>
    </div>
    <SocialMedia />
  </div>
</template>

<script>
import SocialMedia from '@/components/SocialMedia'
export default {
  components: {
    SocialMedia
  },
  async asyncData ({ $content }) {
    const page = await $content('about').fetch()
    return {
      page
    }
  },
  data () {
    return {
      page: null
    }
  }
}
</script>

<style lang="scss" scoped>
.jumbotron {
  color: white;
  background-color: $primary;
  background-image: linear-gradient(rgba(0, 0, 0, 0.65) 0%, rgba(0, 0, 0, 0.65) 100%), url('/img/bg2.jpg');
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

.intro {
  padding: 50px 0 20px;
  text-align: center;
  @include media-breakpoint-up(lg) {
    padding: 70px 0 30px;
  }
  h2 {
    font-weight: 600;
    font-size: 30px;
    max-width: 800px;
    margin: 0 auto 20px;
  }

  p {
    font-size: 17px;
    max-width: 900px;
    margin: 0 auto;
    line-height: 1.7;
    @include media-breakpoint-up(lg) {
      font-size: 19px;
    }
  }
}
p {
  color: rgb(94, 94, 94);
  a {
    color: $secondary;
  }
}
.block {
  text-align: center;
  padding: 30px 0;
  @include media-breakpoint-up(lg) {
    padding: 30px 0 70px;
  }
  .content {
    font-size: 17px;
    line-height: 1.7;
    max-width: 450px;
    margin: 0 auto;
    color: rgb(94, 94, 94);
    /deep/ a {
      color: $secondary;
    }
  }
  h4 {
    color: $secondary;
    font-weight: 600;
    margin-bottom: 15px;
    font-size: 30px;
  }
}
</style>
