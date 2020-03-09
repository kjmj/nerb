<template>
  <div>
    <a
      href="https://www.doordash.com/business/160244/?utm_source=partner-link&utm_medium=website&utm_campaign=160244&utm_content=red-l"
      target="_blank"
      alt="Order Food Delivery with DoorDash"
      title="Order Food Delivery with DoorDash"
      style="text-decoration: none"
      ><div class="doordash">Order Food Delivery with DoorDash</div>
    </a>
    <br />
    <IconButton
      pack="fab"
      icon="facebook"
      size="is-large"
      href="https://www.facebook.com/pages/category/Sandwich-Shop/New-England-Roast-Beef-161820853842034/"
    ></IconButton>
    <IconButton
      pack="fab"
      icon="yelp"
      size="is-large"
      href="https://www.yelp.com/biz/new-england-roast-beef-worcester"
    ></IconButton>
    <IconButton
      pack="fab"
      icon="tripadvisor"
      size="is-large"
      href="https://www.tripadvisor.com/Restaurant_Review-g41952-d854908-Reviews-New_England_Roast_Beef_Incorporated-Worcester_Massachusetts.html"
    ></IconButton>
  </div>
</template>

<script>
import IconButton from './IconButton'
export default {
  name: 'ButtonBar',
  components: { IconButton }
}
</script>

<style scoped>
.doordash {
  position: relative;
  width: 289px;
  height: 59px;
  margin: 0px auto;
  background-image: url(https://cdn.doordash.com/media/button/button_red_l.svg);
  color: transparent;
}
</style>
