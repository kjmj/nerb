<template>
  <section class="section">
    <div id="about" class="container">
      <div class="columns is-centered">
        <div class="column has-text-centered">
          <p class="is-size-3 stripes">
            <span class="bb"
              ><b>Serving Worcester since {{ yearFounded }}</b></span
            >
          </p>
          <p class="is-size-5">Enter a Stranger, leave as a friend</p>
        </div>
      </div>

      <div id="aboutDescription" class="columns is-desktop is-multiline">
        <div class="column is-half-desktop has-text-centered">
          <figure class="image is-16by9">
            <img src="../../static/img/nerbTeam.jpeg" href="Our team" />
          </figure>
        </div>
        <div class="column is-half-desktop has-text-centered">
          <p class="is-size-5">
            We have proudly been serving Worcester for the past
            {{ yearsInBusiness }} years, and pride ourselves in serving the best
            sandwiches in Worcester. Come in today and try one of our delicious
            sandwiches.
          </p>
          <br />
          <p class="is-size-5">
            We also offer catering services, and can accommodate all of your
            needs. We only use the freshest ingredients in our cooking.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {
      yearFounded: 2001
    }
  },
  computed: {
    yearsInBusiness() {
      return new Date(Date.now()).getUTCFullYear() - this.yearFounded
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../static/style';
</style>
