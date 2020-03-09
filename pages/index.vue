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
import NerbHeader from '../components/NerbHeader'
import NerbCarousel from '../components/NerbCarousel'
import About from '../components/About'
import Menu from '../components/Menu'
import NerbInfo from '../components/NerbInfo'
import Footer from '../Components/Footer'

export default {
  name: 'HomePage',
  components: { NerbHeader, NerbCarousel, About, Menu, NerbInfo, Footer }
}
</script>
