<template>
  <b-carousel :pause-info="false">
    <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
      <section
        class="hero is-primary is-medium"
        :style="{
          background: 'url(' + carousel.image + ') center center',
          'background-size': 'cover'
        }"
      >
        <div class="hero-body darkenBackground">
          <div class="container has-text-centered">
            <p class="is-size-1 is-size-3-mobile">
              {{ carousel.title }}
            </p>
            <p class="is-size-4 is-size-6-mobile">{{ carousel.desc }}</p>
            <br />
            <b-button
              v-scroll-to="carousel.scrollToID"
              type="is-primary"
              size="is-medium"
              >{{ carousel.buttonText }}</b-button
            >
          </div>
        </div>
      </section>
    </b-carousel-item>
  </b-carousel>
</template>

<script>
export default {
  name: 'NerbCarousel',
  data() {
    return {
      carousels: [
        {
          title: 'Best Roast Beef in Worcester',
          desc: 'Tender, flavorful, and fresh',
          image: './img/roastBeefSandwich.jpg',
          buttonText: 'View Our Menu',
          scrollToID: '#menuHero'
        },
        {
          title: 'Catering',
          desc: 'We want to cater your next event',
          image: './img/catering.jpg',
          buttonText: 'View Catering Info',
          scrollToID: '#nerbInfo'
        },
        {
          title: 'Fresh Fish & Chips',
          desc: 'Only on Friday',
          image: './img/fishAndChips.jpg',
          buttonText: 'View Our Menu',
          scrollToID: '#menuHero'
        }
      ]
    }
  }
}
</script>

<style scoped>
.darkenBackground {
  background-color: rgba(0, 0, 0, 0.4);
}
</style>
