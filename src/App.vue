<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Main />
    <Foot />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Foot from './components/Foot.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Foot
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
