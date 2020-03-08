<template>
  <div class="columns is-desktop is-multiline">
    <div
      v-for="category in menu"
      :key="category.title"
      class="menu column is-half"
    >
      <p class="title">{{ category.title }}</p>
      <p class="subtitle">{{ category.desc }}</p>
      <div class="menuItem">
        <div class="mainLine">
          <span class="menuColumns"></span>
          <span
            v-for="(col, colIndex) in category.menuColumns"
            :key="colIndex"
            class="price"
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
        <div class="mainLine">
          <span class="name">{{ menuItem.name }}</span>
          <span
            v-for="(price, priceIndex) in menuItem.prices"
            :key="priceIndex"
            class="price"
          >
            {{ price }}
          </span>
        </div>
        <div class="itemDescription">
          {{ menuItem.desc }}
        </div>
      </div>
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

<style scoped type="scss">
.menu {
  /*width: 100%;*/
  padding: 50px 30px;
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
  font-size: 14px;
  font-weight: 500;
  opacity: 0.8;
  margin-bottom: 10px;
}
</style>
