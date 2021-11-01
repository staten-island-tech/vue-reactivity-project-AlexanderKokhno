<template>
  <div id="app">
    <HeaderComp/>
    <DistanceCalc/>
    <InfoComp/>
    <FooterComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import DistanceCalc from './components/DistanceCalc.vue'
import InfoComp from './components/InfoComp.vue'
import FooterComp from './components/FooterComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    DistanceCalc,
    InfoComp,
    FooterComp
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
  background-image:url('./assets/KV-2_abandoned.jpg');
  background-repeat:repeat;
  height: 100rem;
}
</style>
