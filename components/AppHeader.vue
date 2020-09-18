<template>
  <div
    :class="[$route.name, {'nav-open': navOpen }]"
    class="navbar-wrapper"
  >
    <div class="container">
      <div>
        <b-navbar toggleable="lg" type="dark" variant="transparent">
          <b-navbar-brand to="/">
            HealthEat.in
          </b-navbar-brand>

          <b-navbar-toggle target="nav-collapse" @click="toggleMenu" />

          <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
              <b-nav-item to="/">
                Home
              </b-nav-item>
              <b-nav-item to="/about">
                About
              </b-nav-item>
              <b-nav-item to="/recipes">
                Recipes
              </b-nav-item>
              <b-nav-item to="/blog">
                Blog
              </b-nav-item>
              <b-nav-item to="/contact">
                Contact us
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      navOpen: false
    }
  },
  methods: {
    toggleMenu (event) {
      this.navOpen = !this.navOpen
    }
  }
}
</script>

<style lang="scss" scoped>
  .container {
    position: relative;
  }
  .navbar {
    padding: 0.5rem 0;
  }
  .nav-open {
    background-color: rgba(0, 1, 18, 0.8);
    @include media-breakpoint-up(lg) {
      background-color: transparent;
    }
  }

  .navbar-wrapper {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    transition: all 0.5s linear;
    padding-bottom: 25px;

    @include media-breakpoint-up(lg) {
      padding-bottom: 0;
    }
  }

  .navbar-brand {
    font-size: 27px;
    font-weight: 900;
    letter-spacing: 0.3px;

    &:hover {
      color: $secondary;
    }
  }

  .navbar-dark .navbar-toggler {
    color: $white;
    outline: none;
  }

  .navbar-dark .navbar-nav .nav-link {
    font-size: 17px;
    font-weight: 600;
    color: $white;
    @include media-breakpoint-up(lg) {
      padding-right: 0.9rem;
      padding-left: 0.9rem;
    }
    &:hover {
      color: $secondary;
    }
  }
  .navbar-dark .navbar-nav .nav-link.nuxt-link-exact-active {
    color: $secondary;
  }

  .blog-detail,
  .recipes-detail {
    &.navbar-wrapper {
      position: relative;
      background-color: $primary;
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
      padding-bottom: 0;
    }
  }
</style>
