<template>
  <section class="hero is-small is-primary is-bold">
    <div class="hero-body">
      <div class="container has-text-centered">
        <figure class="image has-image-centered" style="max-width: 300px">
          <img src="../static/logo.png" />
        </figure>

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
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.has-image-centered {
  margin-left: auto;
  margin-right: auto;
}
</style>
