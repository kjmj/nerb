<template>
  <div>
    <section id="menuHero" class="hero is-primary is-medium has-bg-img">
      <div class="hero-body">
        <div class="container" style="height: 100px"></div>
      </div>
    </section>
    <div class="container menuContainer">
      <section class="section">
        <div class="columns is-desktop is-multiline">
          <div
            v-for="category in menu"
            :key="category.title"
            class="column is-half-desktop has-text-centered"
          >
            <p class="is-size-4 stripes">
              <span class="bb">
                {{ category.title }}
              </span>
            </p>
            <p class="is-size-6">{{ category.desc }}</p>
            <br />
            <div class="menuItem">
              <div class="mainLine">
                <span class="menuColumns"></span>
                <span
                  v-for="(col, colIndex) in category.menuColumns"
                  :key="colIndex"
                  class="price is-size-6"
                >
                  {{ col }}</span
                >
              </div>
            </div>
            <div
              v-for="menuItem in category.items"
              :key="menuItem.name"
              class="menuItem"
            >
              <div class="mainLine is-size-6">
                <span class="name">{{ menuItem.name }}</span>
                <span
                  v-for="(price, priceIndex) in menuItem.prices"
                  :key="priceIndex"
                  class="price is-size-6"
                >
                  {{ price }}
                </span>
              </div>
              <div class="itemDescription is-size-6">
                {{ menuItem.desc }}
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import nerbMenu from './nerbMenu'

export default {
  name: 'Menu',
  data() {
    return {
      menu: nerbMenu.menu
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../static/style';

.menuContainer {
  width: 80%;
  margin-top: -150px;
  background-color: white;
  z-index: 0;
}

.mainLine {
  display: flex;
}

.name,
.menuColumns {
  margin-right: 0.5em;
  flex: 1;
  display: flex;
}

.name:after {
  content: '';
  border-bottom: dotted 1px;
  flex: 1;
}

.menuColumns:after {
  content: '';
  flex: 1;
}

.price {
  text-align: right;
  flex: 0 0 4em;
}
.itemDescription {
  opacity: 0.8;
  margin-bottom: 10px;
  text-align: left;
}
.has-bg-img {
  background: url('https://shop.guglhupf.com/images/products/kaiser.jpg') center
    center;
  background-size: cover;
}
</style>
