<template>
  <div id="app">
    <MainTop/>
  </div>
</template>

<script>
import MainTop from './components/MainTop.vue'

export default {
  name: 'App',
  components: {
    MainTop
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
