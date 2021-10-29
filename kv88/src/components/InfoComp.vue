<template>
    <div class="InfoDiv">
        <div class="roundType">
            <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
        </div>
        <div id="demoDiv">
          <!-- <div v-if="selected === '400'" id="DDKV">
            <img alt="Vue logo" id="DDKV" v-if="selected === '400'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
            <img alt="Vue logo" id="DDSP" v-else-if="selected === '1100'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
            <img alt="Vue logo" id="DDT34" v-else-if="selected === '950'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
            <img alt="Vue logo" id="DDPL" v-else-if="selected === '1600'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
            <img alt="Vue logo" id="DDT80" v-else-if="selected === '1300'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
          </div>
          <div id="DDKT" v-else-if="selected === '1000'">
            <img alt="Vue logo" id="DDKT"  Src="https://i.pinimg.com/originals/ea/97/89/ea978942986c010e36bb11aa7e9bec14.gif">
          </div> -->
        </div>

    </div>
</template>

<script>
// import { selected } from './components/InfoComp.vue'

export default {
  name: 'InfoDiv',
  props: {
    msg: String
  },
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.DistanceCalcDiv {
  background-color: gray;
  Margin: 5% 10% 5% 10%;
}

#demoDiv {
  margin:2% 5% 2% 5% ;
  justify-content: center;
  background-color: black;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
