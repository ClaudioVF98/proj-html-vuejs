<template>
  <div id="app">
    <MainTop/>
    <MainBot/>
    <BakingOne/>
    <BakingTwo/>
    <BakingThree/>
  </div>
</template>

<script>
import MainTop from './components/MainTop.vue'
import MainBot from './components/MainBot.vue'
import BakingOne from './components/BakingOne.vue'
import BakingTwo from './components/BakingTwo.vue'
import BakingThree from './components/BakingThree.vue'

export default {
  name: 'App',
  components: {
    MainTop,
    MainBot,
    BakingOne,
    BakingTwo,
    BakingThree
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
