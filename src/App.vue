<template>
  <div id="app">
    <FixedComponent/>
    <MainTop/>
    <MainBot/>
    <BakingOne/>
    <BakingTwo/>
    <BakingThree/>
    <LocationAndTimeTable/>
    <ShopContacts/>
    <ShopNow/>
    <MyFooter/>
  </div>
</template>

<script>
import MainTop from './components/MainTop.vue'
import MainBot from './components/MainBot.vue'
import BakingOne from './components/BakingOne.vue'
import BakingTwo from './components/BakingTwo.vue'
import BakingThree from './components/BakingThree.vue'
import LocationAndTimeTable from './components/LocationAndTimeTable.vue'
import ShopContacts from './components/ShopContacts.vue'
import ShopNow from './components/ShopNow.vue'
import MyFooter from './components/MyFooter.vue'
import FixedComponent from './components/FixedComponent.vue'



export default {
  name: 'App',
  components: {
    MainTop,
    MainBot,
    BakingOne,
    BakingTwo,
    BakingThree,
    LocationAndTimeTable,
    ShopContacts,
    ShopNow,
    MyFooter,
    FixedComponent
}
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
