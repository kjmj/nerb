<template>
  <b-carousel :pause-info="false" :autoplay="false">
    <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
      <section
        class="hero is-primary is-medium"
        :style="{
          background: 'url(' + carousel.image + ') center center',
          'background-size': 'cover'
        }"
      >
        <div class="hero-body">
          <div
            class="container has-text-centered"
            style="height: 100px; vertical-align: top"
          >
            <p class="is-size-1">
              {{ carousel.title }}
            </p>
            <p class="is-size-4">{{ carousel.desc }}</p>
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
          title: 'Texas Chicken Melt',
          desc:
            'Grilled chicken onion,peppers, mushrooms BBQ sauce, American Cheese',
          image:
            'http://nerb.publishpath.com/ResizeImage.aspx?m=630&img=%2fWebsites%2fnerb%2fPhotoGallery%2f1393510%2fDSC_8634.jpg&0'
        },
        {
          title: 'Lobster Pita',
          desc: '100% Lobster Meat w/ lettuce, tomato on warm pita bread',
          image:
            'http://nerb.publishpath.com/ResizeImage.aspx?m=630&img=%2fWebsites%2fnerb%2fPhotoGallery%2f1393510%2fDSC_8568.jpg&0'
        },
        {
          title: 'Chicken Bomb',
          desc:
            'Grilled Chicken w/ mushrooms, onion, peppers, jalapenos, American cheese',
          image:
            'http://nerb.publishpath.com/ResizeImage.aspx?m=630&img=%2fWebsites%2fnerb%2fPhotoGallery%2f1393510%2fDSC_8537.jpg&0'
        }
      ]
    }
  }
}
</script>

<style scoped></style>
