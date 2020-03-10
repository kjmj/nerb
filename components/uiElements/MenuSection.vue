<!--This class represents a single section in the menu component-->
<template>
  <div>
    <div class="has-text-centered">
      <p class="is-size-4 stripes">
        <span class="bb">
          <b>{{ section.title }}</b>
        </span>
      </p>
      <p class="is-size-6">{{ section.desc }}</p>
    </div>
    <br />

    <div class="menuItem">
      <div class="mainLine">
        <span class="menuColumns"></span>
        <span
          v-for="(col, colIndex) in section.menuColumns"
          :key="colIndex"
          class="price is-size-6"
        >
          {{ col }}</span
        >
      </div>
    </div>

    <div
      v-for="menuItem in section.items"
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
    <br />
  </div>
</template>

<script>
export default {
  name: 'MenuSection',
  props: {
    section: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../static/style';

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
  flex: 0 0 3.5em;
}
.itemDescription {
  opacity: 0.8;
  margin-bottom: 10px;
  text-align: left;
}
</style>
