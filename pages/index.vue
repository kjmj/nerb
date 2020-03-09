<template>
  <div>
    <NerbHeader></NerbHeader>
    <NerbCarousel></NerbCarousel>
    <About></About>
    <Menu></Menu>
    <NerbInfo></NerbInfo>
    <Footer></Footer>
  </div>
</template>

<script>
import NerbHeader from '../components/sections/NerbHeader'
import NerbCarousel from '../components/sections/NerbCarousel'
import About from '../components/sections/About'
import Menu from '../components/sections/Menu'
import NerbInfo from '../components/sections/NerbInfo'
import Footer from '../components/sections/Footer'

export default {
  name: 'HomePage',
  components: { NerbHeader, NerbCarousel, About, Menu, NerbInfo, Footer }
}
</script>
