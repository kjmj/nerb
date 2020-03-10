<template>
  <div>
    <section id="menuHero" class="hero is-primary is-medium has-bg-img">
      <div class="hero-body">
        <div class="container" style="height: 100px"></div>
      </div>
    </section>
    <div class="container menuContainer">
      <section class="section">
        <!--The idea is to create two columns-->
        <!--We fill the columns with "MenuSection" components, each representing a section of the menu (i.e. Appetizers, Sandwiches, Desserts)-->
        <!--This way, there is no vertical space wasted between row elements in the columns-->
        <div class="columns is-desktop is-multiline">
          <div class="column is-half-desktop has-text-centered">
            <MenuSection
              v-for="section in first"
              :key="section.title"
              :section="section"
            ></MenuSection>
          </div>
          <div class="column is-half-desktop has-text-centered">
            <MenuSection
              v-for="section in second"
              :key="section.title"
              :section="section"
            ></MenuSection>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import MenuSection from '../uiElements/MenuSection'
import nerbMenu from './nerbMenu'

export default {
  name: 'Menu',
  components: { MenuSection },
  data() {
    return {
      first: nerbMenu.menu.firstHalf,
      second: nerbMenu.menu.secondHalf
    }
  }
}
</script>

<style scoped lang="scss">
.menuContainer {
  width: 80%;
  margin-top: -150px;
  background-color: white;
  z-index: 0;
}
.has-bg-img {
  background: url('../../static/img/rolls.jpg') center center;
  background-size: cover;
}
</style>
