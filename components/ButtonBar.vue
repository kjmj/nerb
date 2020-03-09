<template>
  <div>
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
  width: 209px;
  height: 45px;
  margin: 0px auto;
  background-image: url(https://cdn.doordash.com/media/button/button_red_m.svg);
  color: transparent;
}
</style>
