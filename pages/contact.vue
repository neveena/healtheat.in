<template>
  <div>
    <div class="jumbotron jumbotron-fluid">
      <b-container>
        <h1 class="font-weight-bold">
          Contact us
        </h1>
      </b-container>
    </div>
    <div class="contact-details">
      <b-container>
        <b-row>
          <b-col md="6">
            <h4>
              Any orders can be placed from Monday to Friday. Delivered on Saturday/Sunday
            </h4>
            <p>
              We love our customers, so feel free to Call or Whatsapp with any query, prices or to place orders.
            </p>
            <a href="https://wa.me/919886090888" target="_blank" class="mt-2 btn btn-green">
              <IconWhatsapp />
              Message us on WhatsApp
            </a>
            <h4>Healtheat</h4>
            <p>
              Indiranagar, Chinmaya Mission Hospital Road, Binnamangala, Stage 1, Indiranagar, Bengaluru, Karnataka, India
            </p>
            <a href="tel:9886090888">9886090888</a>/<a href="mailto:Hello@healtheat.in">Hello@healtheat.in</a>
            <h4>Hours</h4>
            <div v-b-toggle.collapse-1 variant="primary" class="hours">
              Open today <span class="time">{{ getTodayOpeningHours[0].label }}</span>
              <img src="/down-chevron.svg" width="15px" class="ml-3">
            </div>
            <b-collapse id="collapse-1" class="mt-2">
              <table class="table table-bordered">
                <tbody>
                  <tr
                    v-for="hour in openingHours"
                    :key="hour.value"
                    :class="{ 'today': getTodayOpeningHours[0].value === hour.value}"
                  >
                    <th>
                      {{ hour.day }}
                    </th>
                    <td>{{ hour.label }}</td>
                  </tr>
                </tbody>
              </table>
            </b-collapse>
          </b-col>
          <b-col md="6" class="mt-4">
            <iframe
              width="100%"
              height="400px"
              frameborder="0"
              scrolling="no"
              marginheight="0"
              marginwidth="0"
              src="https://www.openstreetmap.org/export/embed.html?bbox=77.6377269916702%2C12.977535491250238%2C77.63993176748048%2C12.979349392806368&amp;layer=mapnik&amp;marker=12.978442443682688%2C77.63882937957533"
            />
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

  data () {
    return {
      openingHours: [
        {
          value: 1,
          day: 'Mon',
          label: '09:00 am – 05:00 pm'
        },
        {
          value: 2,
          day: 'Tue',
          label: '09:00 am – 05:00 pm'
        },
        {
          value: 3,
          day: 'Wed',
          label: '09:00 am – 05:00 pm'
        },
        {
          value: 4,
          day: 'Thu',
          label: '09:00 am – 05:00 pm'
        },
        {
          value: 5,
          day: 'Fri',
          label: '09:00 am – 05:00 pm'
        },
        {
          value: 6,
          day: 'Sat',
          label: 'Closed'
        },
        {
          value: 7,
          day: 'Sun',
          label: 'Closed'
        }
      ]
    }
  },

  computed: {
    getDay () {
      return new Date().getDay()
    },

    getTodayOpeningHours () {
      return this.openingHours.filter((hour) => {
        return hour.value === this.getDay
      })
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

h4 {
  font-size: 22px;
  font-weight: 600;
}

p {
  color: rgb(94, 94, 94);
  font-size: 16px;
  margin-bottom: 24px;
}

a {
  color: $secondary;
  display: inline-block;
  margin-bottom: 24px;
}

.btn-green {
  background-color: #455a64;
  border-radius: 0;
  padding: 15px 15px;
  color: $white;
  border-radius: 10px;
  margin-bottom: 24px;
  &:hover {
    background-color: #64b161;
  }
}

.contact-details {
  padding: 40px 0;
  @include media-breakpoint-up(lg) {
    padding: 70px 0;
  }
}

.hours {
  outline: none;
}
.time {
  color: $secondary;
  font-weight: 700;
}
.today {
  font-weight: 900;
  background-color: lighten($secondary, 40%);
}
</style>
