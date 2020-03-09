<template>
  <div>
    <About></About>
    <Menu></Menu>
    <NerbInfo></NerbInfo>
  </div>
</template>

<script>
import About from '../components/About'
import Menu from '../components/Menu'
import NerbInfo from '../components/NerbInfo'
export default {
  name: 'HomePage',
  components: { NerbInfo, Menu, About }
}
</script>
