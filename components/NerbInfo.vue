<template>
  <section class="section">
    <div id="nerbInfo" class="container nerbInfoContainer">
      <div class="columns is-desktop is-multiline">
        <div class="info column is-half-desktop has-text-centered">
          <p class="is-size-4">Location</p>
          <p>{{ location.address }}</p>
          <p>{{ location.city }}, {{ location.state }} {{ location.zip }}</p>
          <p>{{ location.phone }}</p>
          <br />
          <p class="is-size-4">Hours</p>
          <p v-for="(item, index) in hours" :key="index">
            <b>{{ item.day }}:</b> {{ item.hours }}
          </p>

          <section class="section">
            <IconButton
              icon="facebook"
              size="is-large"
              href="https://www.facebook.com/pages/category/Sandwich-Shop/New-England-Roast-Beef-161820853842034/"
            ></IconButton>
            <IconButton
              icon="yelp"
              size="is-large"
              href="https://www.yelp.com/biz/new-england-roast-beef-worcester"
            ></IconButton>

            <a
              href="https://www.doordash.com/business/160244/?utm_source=partner-link&utm_medium=website&utm_campaign=160244&utm_content=red-m"
              target="_blank"
              alt="Order Food Delivery with DoorDash"
              title="Order Food Delivery with DoorDash"
              style="text-decoration: none"
              ><div class="doordash">
                Order Food Delivery with DoorDash
              </div>
            </a>
          </section>
        </div>
        <div class="info column is-half-desktop has-text-centered">
          <section class="section">
            <p>Map here</p>
          </section>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import IconButton from './IconButton'
export default {
  name: 'NerbInfo',
  components: { IconButton },
  data() {
    return {
      hours: [
        {
          day: 'Monday - Friday',
          hours: '10am to 10pm'
        },
        {
          day: 'Saturday',
          hours: '10am to 9pm'
        },
        {
          day: 'Sunday',
          hours: 'Closed'
        }
      ],
      location: {
        address: '33 Park Avenue',
        city: 'Worcester',
        state: 'MA',
        zip: '01605-3910',
        phone: '508.756.1991'
      }
    }
  }
}
</script>

<style scoped>
.nerbInfoContainer {
  width: 80%;
}

.info {
  padding: 0 30px;
}

.doordash {
  position: relative;
  width: 209px;
  height: 45px;
  margin: 0px auto;
  background-image: url(https://cdn.doordash.com/media/button/button_red_m.svg);
  color: transparent;
}
</style>
