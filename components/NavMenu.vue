<template>
  <ul>
    <li>
      <a v-scroll-to="'#about'">About</a>
    </li>
    <li>
      <a v-scroll-to="'#menuHero'">Menu</a>
    </li>
    <li>
      <a v-scroll-to="'#nerbInfo'">Contact</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'NavMenu'
}
</script>

<style scoped lang="scss">
@import '../static/style';

$duration: 0.2s;
$distance: 8px;
$easeOutBack: cubic-bezier(0.175, 0.885, 0.32, 1.275);

body {
  background-color: $light;
}

ul {
  list-style-type: none;
  margin: 0;
  text-align: center;

  li {
    display: inline-block;
    margin: 0 20px;
  }
}

a {
  color: $dark;
  position: relative;
  text-transform: uppercase;
  text-decoration: none;
  padding-bottom: 8px;

  &:before,
  &:after {
    content: '';
    position: absolute;
    bottom: 2px;
    left: 0;
    right: 0;
    height: 2px;
    background-color: $primary;
  }
  &:before {
    opacity: 0;
    transform: translateY(-$distance);
    transition: transform 0s $easeOutBack, opacity 0s;
  }
  &:after {
    opacity: 0;
    transform: translateY($distance/2);
    transition: transform $duration $easeOutBack, opacity $duration;
  }
  &:hover,
  &:focus {
    &:before,
    &:after {
      opacity: 1;
      transform: translateY(0);
    }
    &:before {
      transition: transform $duration $easeOutBack, opacity $duration;
    }
    &:after {
      transition: transform 0s $duration $easeOutBack, opacity 0s $duration;
    }
  }
}
</style>
