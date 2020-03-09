<template>
  <div>
    <NerbHeader></NerbHeader>
    <About></About>
    <Menu></Menu>
    <NerbInfo></NerbInfo>
    <Footer></Footer>
  </div>
</template>

<script>
import NerbHeader from '../components/NerbHeader'
import About from '../components/About'
import Menu from '../components/Menu'
import NerbInfo from '../components/NerbInfo'
import Footer from '../Components/Footer'

export default {
  name: 'HomePage',
  components: { NerbHeader, About, Menu, NerbInfo, Footer }
}
</script>
