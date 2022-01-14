<template>
  <div id="app">
    <Header />
    <Main />
    <Foot />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Foot from './components/Foot.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Foot
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
