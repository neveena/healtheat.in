<template>
  <div class="social-media">
    <b-container>
      <div class="title">
        <h2>We're social</h2>
        <p>Join us on facebook & instagram</p>
      </div>
      <div class="d-flex justify-content-center">
        <a href="https://www.facebook.com/healtheat.in" target="_blank" class="mr-4 fb">
          <Facebook />
        </a>
        <a href="https://www.instagram.com/healtheat.in" target="_blank" class="insta">
          <Instagram />
        </a>
      </div>
    </b-container>
  </div>
</template>

<script>
import Facebook from '@/components/icons/Facebook'
import Instagram from '@/components/icons/Instagram'

export default {
  components: {
    Facebook,
    Instagram
  }
}
</script>
<style lang="scss" scoped>
.social-media {
  padding: 60px 0 70px;
  background-color: #f6f6f6;
  .title {
    text-align: center;
    margin-bottom: 50px;
    h2 {
      color: $secondary;
      font-size: 38px;
      font-weight: 900;
      position: relative;

      @include media-breakpoint-up(md) {
        font-size: 40px;
      }

      @include media-breakpoint-up(lg) {
        font-size: 48px;
      }
    }

    p {
      font-size: 18px;
      color: rgb(94, 94, 94);

      @include media-breakpoint-up(lg) {
        font-size: 21px;
      }
    }
  }

  .insta svg {
    width: 57px;
    margin-right: 5px;
  }
  .fb svg {
    width: 55px;
    margin-right: 5px;
  }
}
</style>
