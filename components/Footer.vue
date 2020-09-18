<template>
  <footer id="dk-footer" class="dk-footer">
    <div class="container">
      <div class="row">
        <div class="col-md-12 col-lg-4">
          <div>
            <a href="/" class="footer-logo">
              HealthEat.in
            </a>
          </div>
        </div>
        <!-- End Col -->
        <div class="col-md-12 col-lg-8">
          <div class="row">
            <div class="col-md-7">
              <div class="contact-us">
                <div class="contact-icon">
                  <Map />
                </div>
                <a class="contact-info" href="https://www.google.com/maps?daddr=Indiranagar,+Chinmaya+Mission+Hospital+Road,+Binnamangala,+Stage+1,+Indiranagar,+Bengaluru,+Karnataka,+India" target="_blank">
                  <h3>Bengaluru, Karnataka, India</h3>
                  <p>Chinmaya Mission Hospital Road, Binnamangala, Stage 1, Indiranagar</p>
                </a>
              </div>
            </div>
            <div class="col-md-4">
              <div class="contact-us contact-us-last">
                <div class="contact-icon">
                  <Call />
                </div>
                <a class="contact-info" href="tel:9886090888">
                  <h3>9886090888</h3>
                  <p>Give us a call</p>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="copyright">
      <div class="container">
        <div class="row">
          <div class="col-md-6">
            <span>Copyright © {{ getYear }}, All Right Reserved HealthEat.in</span>
          </div>
          <div class="col-md-6 text-right">
            <span><a href="http://neveenaferrao.netlify.app/" target="_blank">Designed by: neveena</a></span>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Call from '@/components/icons/Call'
import Map from '@/components/icons/Map'

export default {
  components: {
    Call,
    Map
  },
  computed: {
    getYear () {
      const currentDate = new Date()
      return currentDate.getFullYear()
    }
  }
}
</script>

<style lang="scss" scoped>
p {
  /* font-family: 'Nunito', sans-serif; */
  font-size: 16px;
  line-height: 28px;
}

.footer-logo {
  font-size: 40px;
  color: white;
  font-weight: 900;
  margin-bottom: 20px;
  display: block;
  text-decoration: none;

  &:hover {
    color: $secondary;
  }
}

.dk-footer {
  padding: 30px 0 0;
  background-color: #151414;
  position: relative;
  z-index: 2;
  text-align: center;
  @include media-breakpoint-up(md) {
    text-align: left;
  }
  @include media-breakpoint-up(lg) {
    padding: 70px 0 0;
  }
}

.dk-footer-box-info {
  background: #202020;
  padding: 40px;
  color: #fff;
}

.footer-info-text {
  margin: 26px 0 32px;
}

.contact-us {
  position: relative;
  display: flex;
  flex-direction: column;
  @include media-breakpoint-up(md) {
    flex-direction: row;
  }
}

.contact-icon {
  margin-bottom: 15px;
  @include media-breakpoint-up(md) {
    margin-bottom: 0;
    margin-right: 30px;
  }
}

.contact-info {
  text-decoration: none;
  color: #fff;
}

 a.contact-info:hover {
  color: $secondary;
}

.contact-info h3 {
  font-size: 20px;
  margin-bottom: 0;
}

.copyright {
  padding: 28px 0;
  margin-top: 55px;
  background-color: #202020;
}

.copyright span,
.copyright a {
  color: #878787;
  transition: all 0.3s linear;
}

.copyright a:hover {
  color: $secondary;
}

.contact-icon svg {
  width: 30px;
  fill: $secondary;
}
</style>
