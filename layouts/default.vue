<template>
  <div>
    <section class="hero is-medium is-primary is-bold">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title">
            New England Roast Beef
          </h1>
          <h2 class="subtitle">
            Serving the best sandwiches in Worcester
          </h2>
          <br />
          <a v-scroll-to="'#about'" style="color: white">About</a>
          <a v-scroll-to="'#menuHero'" style="color: white">Menu</a>
          <a v-scroll-to="'#nerbInfo'" style="color: white">Contact</a>
        </div>
      </div>
    </section>

    <nuxt />
    <div style="height: 1000px"></div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
@import '../static/style';
</style>
