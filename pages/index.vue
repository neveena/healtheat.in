<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <div class="container">
        <h1 class="font-weight-bold">
          Dry Fruits, Spices & more...
        </h1>
        <p class="mb-4">
          Fresh and organically sourced
        </p>
        <nuxt-link to="/contact" class="btn btn-secondary">
          Contact us
        </nuxt-link>
      </div>
    </div>

    <div class="introduction">
      <b-container>
        <b-row class="align-items-center">
          <b-col md="6">
            <img src="/img/14.jpg">
          </b-col>

          <b-col md="6">
            <div class="block-title">
              <small>HealthEat.in</small>
              <h2>Welcome</h2>
            </div>
            <div class="block-content">
              <p>
                We are a bunch of young health and fitness enthusiasts doing our bit to make Bengaluru a tad bit healthier.
              </p>
              <p>
                All varieties of Organically sourced Dry fruits (Almonds, Cashews, Raisins, Figs, walnuts, dates etc..) and spices are available.
              </p>
              <p>
                Place your orders via call or WhatsApp.
              </p>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>

    <div class="product-category">
      <b-container>
        <div class="title">
          <h2>Product Category</h2>
          <p>We sell only Premium to Hybrid export quality dry fruits and spices.</p>
        </div>
        <b-row>
          <b-col md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" src="/img/product/nuts.jpg" alt="Nuts & Dried fruits">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  Nuts & Dried fruits
                </h5>
                <p class="card-text">
                  Organically sourced and procured from the origin.
                </p>
                <!-- <a href="#" class="btn btn-secondary">Contact us</a> -->
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" src="/img/product/spices.jpg" alt="Spices">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  Spices
                </h5>
                <p class="card-text">
                  All Natural high quality spices
                </p>
                <!-- <a href="#" class="btn btn-secondary">Contact us</a> -->
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" src="/img/product/honey.jpg" alt="Honey">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  Honey
                </h5>
                <p class="card-text">
                  100% Natural and pure honey. (Lab tested)
                </p>
                <!-- <a href="#" class="btn btn-secondary">Contact us</a> -->
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" src="/img/product/coffee.jpg" alt="Coffee Powder">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  Coffee Powder
                </h5>
                <p class="card-text">
                  Arriving Soon...
                </p>
                <!-- <a href="#" class="btn btn-secondary">Contact us</a> -->
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-5">
            <div class="card">
              <div class="image-wrapper">
                <img class="card-img-top" src="/img/product/chocolate.jpg" alt="Home Made Chocolates">
              </div>
              <div class="card-body">
                <h5 class="card-title">
                  Home Made Chocolates
                </h5>
                <p class="card-text">
                  Arriving Soon...
                </p>
                <!-- <a href="#" class="btn btn-secondary">Contact us</a> -->
              </div>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>

    <div class="cta">
      <b-container>
        To place orders Call us at
        <a href="tel:9886090888">9886090888</a>
        <br>
        or
        <br>
        <a href="https://wa.me/919886090888" target="_blank" class="mt-2 btn btn-green">
          <IconWhatsapp />
          Message us on WhatsApp
        </a>
      </b-container>
    </div>

    <div class="gift-box">
      <b-container>
        <b-row class="align-items-center">
          <b-col md="6">
            <div class="block-title">
              <small>HealthEat.in</small>
              <h2>Gift box</h2>
            </div>
            <div class="block-content">
              <p>
                Send a gift Box through us to friends and family or buy it now to gift your loved ones.
              </p>
              <p>
                Just call us or whatsapp for details and gifting options.
              </p>
            </div>
          </b-col>
          <b-col md="6">
            <img src="/img/gift-box.jpg">
          </b-col>
        </b-row>
      </b-container>
    </div>

    <div class="how-it-works">
      <b-container>
        <b-row class="align-items-center">
          <b-col md="6">
            <img src="/img/how-does-it-work.jpg">
          </b-col>

          <b-col md="6">
            <div class="block-title">
              <small>HealthEat.in</small>
              <h2>How it works</h2>
            </div>
            <div class="block-content">
              <p>
                <span class="font-weight-bold">Call/Whatsapp us for price list & to place order.</span> <br>(Shelf life of naturally dried fruits are 2 to 3 months, hence we procure fresh stock every week as per the orders received)
              </p>
              <p class="font-weight-bold">
                Once the order is received, we will deliver the product to you during the weekend.
              </p>
              <p class="font-weight-bold">
                Payment to be done on delivery by cash/Gpay or online transfer.
              </p>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>

    <SocialMedia />
  </div>
</template>

<script>
import IconWhatsapp from '@/components/icons/Whatsapp'
import SocialMedia from '@/components/SocialMedia'

export default {
  components: {
    SocialMedia,
    IconWhatsapp
  },
  head () {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
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
  padding: 90px 0 70px;
  @include media-breakpoint-up(lg) {
    min-height: 440px;
    height: 70vh;
    padding: 0;
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

.block-title {
  small {
    font-size: 14px;
    color: rgb(94, 94, 94);
    margin-bottom: 5px;
    display: block;
  }

  h2 {
    font-size: 38px;
    font-weight: 900;
    margin-bottom: 20px;
    @include media-breakpoint-up(md) {
      font-size: 40px;
    }

    @include media-breakpoint-up(lg) {
      font-size: 48px;
    }
  }
}

.block-content p {
  font-size: 18px;
  color: rgb(94, 94, 94);

  @include media-breakpoint-up(lg) {
    font-size: 21px;
  }
}

.introduction {
  padding: 70px 0;

  img {
    display: none;

    @include media-breakpoint-up(md) {
      display: block;
    }
    @include media-breakpoint-up(lg) {
      padding-right: 40px;
    }
  }
}

.product-category {
  padding: 70px 0;
  background-color: #f6f6f6;
  .card {
    height: 100%;
    .image-wrapper {
      height: 232px;
      overflow: hidden;
    }
    .card-img-top {
      max-height: 100%;
      object-fit: cover;
      object-position: center;
    }
    h5 {
      font-weight: 600;
    }
    p {
      color: rgb(94, 94, 94);
    }
  }
}

.cta {
  padding: 40px 0;
  background-color: $primary;
  color: $white;
  font-size: 25px;
  text-align: center;

  a {
    color: $secondary;
    display: inline-block;
  }

  .btn-green {
    background-color: #455a64;
    border-radius: 0;
    padding: 15px 15px;
    color: $white;
    &:hover {
      background-color: #64b161;
    }
  }
}

.gift-box {
  padding: 60px 0 30px;
  text-align: center;
  @include media-breakpoint-up(md) {
    text-align: left;
  }
}

.how-it-works {
  padding: 40px 0 90px;
  text-align: center;
  @include media-breakpoint-up(md) {
    text-align: left;
  }
}

</style>
