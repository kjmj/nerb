<template>
  <div id="nerbInfo" class="container nerbInfoContainer has-text-centered">
    <p class="is-size-3 stripes">
      <span class="bb">Get in Touch</span>
    </p>
    <br />
    <br />
    <div class="columns is-desktop is-multiline">
      <div class="info column is-half-desktop">
        <p class="is-size-4"><b>Catering</b></p>
        <p>Please call Cathy at 603.966.6339</p>
        <br />
        <p class="is-size-4"><b>Location</b></p>
        <p>{{ location.address }}</p>
        <p>{{ location.city }}, {{ location.state }} {{ location.zip }}</p>
        <p>{{ location.phone }}</p>
        <br />
        <p class="is-size-4"><b>Hours</b></p>
        <p v-for="(item, index) in hours" :key="index">
          <b>{{ item.day }}:</b> {{ item.hours }}
        </p>
        <br />
        <ButtonBar></ButtonBar>
        <br />
      </div>

      <div class="info column is-half-desktop has-text-centered">
        <NerbMap></NerbMap>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonBar from '../uiElements/ButtonBar'
import NerbMap from '../uiElements/NerbMap'
export default {
  name: 'NerbInfo',
  components: { NerbMap, ButtonBar },
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

<style scoped lang="scss">
@import '../../static/style';
.nerbInfoContainer {
  width: 80%;
}

.info {
  padding: 0 30px;
}
</style>
