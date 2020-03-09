<template>
  <div>
    <Header></Header>
    <About></About>
    <Menu></Menu>
    <NerbInfo></NerbInfo>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '../Components/Header'
import About from '../components/About'
import Menu from '../components/Menu'
import NerbInfo from '../components/NerbInfo'
import Footer from '../Components/Footer'

export default {
  name: 'HomePage',
  components: { Header, About, Menu, NerbInfo, Footer }
}
</script>
