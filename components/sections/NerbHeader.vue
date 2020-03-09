<template>
  <section class="hero is-small">
    <div class="hero-body">
      <div class="container has-text-centered">
        <figure class="image has-image-centered" style="max-width: 300px">
          <img src="../../static/logo.png" />
        </figure>

        <h2 class="is-size-5">
          Serving the best sandwiches in Worcester
        </h2>
        <br />
        <br />

        <NavMenu></NavMenu>
      </div>
    </div>
  </section>
</template>

<script>
import NavMenu from '../uiElements/NavMenu'
export default {
  name: 'NerbHeader',
  components: { NavMenu }
}
</script>

<style scoped lang="scss">
.has-image-centered {
  margin-left: auto;
  margin-right: auto;
}
</style>
