<template>
  <div id="app">
    <HeaderComp/>
    <DistanceCalc/>
    <InfoComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import DistanceCalc from './components/DistanceCalc.vue'
import InfoComp from './components/InfoComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    DistanceCalc,
    InfoComp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-image:url('https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif');
  background-repeat:repeat;
  height: 100rem;
}
</style>
