<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <b-container>
        <h1 class="font-weight-bold">
          Offers
        </h1>
      </b-container>
    </div>

    <div class="offers-list">
      <b-container>
        <b-row>
          <b-col md="6" lg="4" class="mb-3">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">
                  Special title
                </h5>
                <p class="card-text">
                  With supporting text below as a natural lead-in to additional content.
                </p>
              </div>
              <div class="card-footer text-muted">
                2 days ago
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-3">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">
                  Special title treatment
                </h5>
                <p class="card-text">
                  With supporting text below as a natural lead-in to additional content.
                </p>
              </div>
              <div class="card-footer text-muted">
                2 days ago
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-3">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">
                  Special title treatment
                </h5>
                <p class="card-text">
                  With supporting text.
                </p>
              </div>
              <div class="card-footer text-muted">
                10 days ago
              </div>
            </div>
          </b-col>
          <b-col md="6" lg="4" class="mb-3">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">
                  Special title treatment
                </h5>
                <p class="card-text">
                  With supporting text below as a natural lead-in to additional content.
                </p>
              </div>
              <div class="card-footer text-muted">
                2 days ago
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
  background-image: linear-gradient(rgba(0, 0, 0, 0.65) 0%, rgba(0, 0, 0, 0.65) 100%), url('/img/12.jpg');
  background-position: bottom center;
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
.offers-list {
  padding: 40px 0;
  @include media-breakpoint-up(lg) {
    padding: 70px 0;
  }
}

.card {
  height: 100%;

  h5 {
    color: $secondary;
    font-weight: 700;
    font-size: 23px;
  }
}
</style>
