<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <b-container>
        <h1 class="font-weight-bold">
          Our Recipes
        </h1>
      </b-container>
    </div>
    <div class="recipe-list">
      <b-container>
        <b-row>
          <b-col md="6">
            <div class="card mb-4">
              <div class="card-block">
                <h4 class="card-title">
                  Lorem ipsum dolor sit amet
                </h4>
                <p class="card-text">
                  Consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </p>
                <a href="#" class="link">Read More</a>
              </div>
            </div>
          </b-col>
          <b-col md="6">
            <div class="card mb-4">
              <div class="card-block">
                <h4 class="card-title">
                  Lorem ipsum dolor sit amet
                </h4>
                <p class="card-text">
                  Consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </p>
                <a href="#" class="link">Read More</a>
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
  components: {
  }
}
</script>

<style lang="scss" scoped>
.jumbotron {
  color: white;
  background-color: $primary;
  background-image: linear-gradient(rgba(0, 0, 0, 0.65) 0%, rgba(0, 0, 0, 0.65) 100%), url('/img/bg3.jpg');
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
.recipe-list {
  padding: 40px 0;
  @include media-breakpoint-up(lg) {
    padding: 70px 0;
  }
  .card-title {
    margin-bottom: 5px;
    font-size: 22px;
    font-weight: 700;
  }
  .card-block {
    padding: 20px;
  }
  .link {
    color: $secondary;
    font-weight: 700;
  }
  p {
    margin-bottom: 10px;
  }
}

</style>
