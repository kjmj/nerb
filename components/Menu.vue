<template>
  <div>
    <div v-for="category in menu" :key="category" class="menu">
      <p class="title">{{ category.title }}</p>
      <p class="subtitle">{{ category.desc }}</p>
      <div class="menuItem">
        <div class="mainLine">
          <span class="columns"></span>
          <span v-for="col in category.columns" :key="col" class="price">{{
            col
          }}</span>
        </div>
      </div>
      <div v-for="menuItem in category.items" :key="menuItem" class="menuItem">
        <div class="mainLine">
          <span class="name">{{ menuItem.name }}</span>
          <span v-for="price in menuItem.prices" :key="price" class="price">{{
            price
          }}</span>
        </div>
        <div class="description">
          {{ menuItem.desc }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data() {
    return {
      menu: [
        {
          title: 'Specialty Sandwiches',
          desc:
            "New England Roast Beef's Specialty Sandwiches are available on the following bread: french white, french wheat, white wrap, wheat wrap,spinach wrap, sliced wheat, sliced light rye, sliced dark rye and pita bread. Make any sandwich a combo meal for $4.00, includes fries, onion rings and cole slaw.",
          columns: [],
          items: [
            {
              name: 'Original Philly Beef Steak Bomb',
              prices: ['9.99'],
              desc: 'Jalapenos, onions, peppers, mushrooms, American cheese'
            },
            {
              name: ' Original Philly Beef Cheese Steak',
              prices: ['9.99'],
              desc: 'Onions, peppers & American cheese'
            }
          ]
        },
        {
          title: 'Chicken Specialty Sandwiches',
          desc:
            "New England Roast Beef's Chicken Specialty Sandwiches are available on the following bread: french white, french wheat, white wrap, wheat wrap,spinach wrap, sliced wheat, sliced light rye, sliced dark rye and pita bread. Make any sandwich a combo meal for $4.00 beer battered  fries, beer battered onion rings and cole slaw.",
          columns: [],
          items: [
            {
              name: 'BBQ Chicken',
              prices: ['9.99'],
              desc: 'White Chicken marinated BBQ sauce, lettuce & tomatoes'
            },
            {
              name: 'Buffalo Chicken',
              prices: ['9.99'],
              desc:
                'Grilled white chicken with buffalo sauce, lettuce, tomatoes & bleu cheese'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style type="scss">
.menu {
  width: 100%;
  padding: 50px 30px;
}

.mainLine {
  display: flex;
}

.name,
.columns {
  margin-right: 0.5em;
  flex: 1;
  display: flex;
}

.name:after {
  content: '';
  border-bottom: dotted 1px;
  flex: 1;
}

.columns:after {
  content: '';
  flex: 1;
}

.price {
  text-align: right;
  flex: 0 0 4em;
}
.description {
  font-size: 14px;
  font-weight: 500;
  opacity: 0.8;
  margin-bottom: 10px;
}
</style>
