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
          <a v-scroll-to="'#about'" href="#" style="color: white">About</a>
          <a v-scroll-to="'#menuHero'" href="#" style="color: white">Menu</a>
          <a v-scroll-to="'#element'" href="#" style="color: white">Contact</a>
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
// Change default font
@import url('https://fonts.googleapis.com/css?family=Lora:400,500&subset=cyrillic');
$family-sans-serif: 'Lora', sans-serif;

// Import Bulma's core
@import '~bulma/sass/utilities/_all';

// Import Bulma and Buefy styles
@import '~bulma';
@import '~buefy/src/scss/buefy';
</style>
