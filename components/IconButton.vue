<!--An IconButton component. Has a custom hover effect.-->
<template>
  <a :href="href" target="_blank">
    <b-icon :pack="pack" :icon="icon" :size="size"></b-icon>
  </a>
</template>

<script>
export default {
  name: 'IconButton',
  props: {
    pack: {
      type: String,
      default: 'fas'
    },
    icon: {
      type: String,
      default: 'cursor-default'
    },
    size: {
      type: String,
      default: 'is-large'
    },
    href: {
      type: String,
      default: '#'
    }
  }
}
</script>

<style scoped lang="scss">
@import '../static/bulmaStyle';

a {
  background-color: $dark;
  border-radius: 50%;
  border: none;
  color: $light;
  padding: 5px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 4px;
  transition: 0.5s;
}

a:hover {
  color: $primary;
}
</style>
