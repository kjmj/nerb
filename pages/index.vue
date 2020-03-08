<template>
  <div>
    <About></About>
    <Menu></Menu>
  </div>
</template>

<script>
import About from '../components/About'
import Menu from '../components/Menu'
export default {
  name: 'HomePage',
  components: { Menu, About }
}
</script>
