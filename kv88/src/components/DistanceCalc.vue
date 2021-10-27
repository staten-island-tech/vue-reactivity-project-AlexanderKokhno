<template>
    <div class="DistanceCalcDiv">
        <div class="roundType">
            <p>Select Round (mm)(name)(type)
            </p>
            <!-- <form>
                <select name="ShellDPn" id="ShellDPn" v-on:change="Calc_Distance" >
                    <option id="PLCH" selected>Select Shell Type Here</option>
                    <option value="KLm" id="KV_AC" v-on:click="testfunc1">{{STA1[0]}}</option>
                    <option value="OBm" id="OB_MU">{{STA1[1]}}</option>
                    <option value="MLm" id="ML_MU">{{STA1[2]}}</option>
                    <option value="MLm2" id="ML_MU2">{{STA1[3]}}</option>
                    <option value="MLm3" id="ML_MU3">{{STA1[4]}}</option>
                    <option value="MLm4" id="ML_MU4">{{STA1[5]}}</option>
                </select>
            </form> -->
            <div>
              <button @click="dropDown">Calculate</button>
              <select v-model="selected" class="form-control sl">
              <option v-for="option in options" :value="option.value" :key="option.value">{{ option.name }}</option>
              </select>
            </div>
            <!-- <button v-on:click="Calc_Distance" id="Calc_Btn">Calculate2</button> -->
        </div>
        <div id="demoDiv">
          <img alt="Vue logo" id="DDKV" v-if="selected === '400'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
          <img alt="Vue logo" id="DDKT" v-else-if="selected === '1000'" Src="https://i.pinimg.com/originals/ea/97/89/ea978942986c010e36bb11aa7e9bec14.gif">
          <img alt="Vue logo" id="DDSP" v-else-if="selected === '1100'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
          <img alt="Vue logo" id="DDT34" v-else-if="selected === '950'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
          <img alt="Vue logo" id="DDPL" v-else-if="selected === '1600'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
          <img alt="Vue logo" id="DDT80" v-else-if="selected === '1300'" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
        </div>

    </div>
</template>

<script>
export default {
  name: 'DistanceCalc',
  props: {
    msg: String
  },
  data () {
    return {
      testvar1: 5,
      testvar2: 5.5,
      testvar3: 6.43442,
      distance: 0,
      // STA1:
      // ['152mm G-530 - The Anti-Concrete', '88mm (PzGr 39/43) - APCBC', '128mm 12,8/8,8 Pzgr.TS - APCBC', '120mm T14E3 - APCBC', '120mm DM43 - APFSDS', '120mm 3BK18M - HEATFS'
      // ],
      // gei_kv2_ac: document.getElementById('KV_AC')
      options: [],
      selected: ''
    }
  },
  methods: {
    dropDown: function () {
      var DDFV = this
      var types = [
        {
          name: '152mm G-530 - The Anti-Concrete',
          value: '400'
        },
        {
          name: '88mm (PzGr 39/43) - APCBC',
          value: '1000'
        },
        {
          name: '128mm 12,8/8,8 Pzgr.TS - APCBC',
          value: '1100'
        },
        {
          name: '120mm T14E3 - APCBC',
          value: '950'
        },
        {
          name: '120mm DM43 - APFSDS',
          value: '1600'
        },
        {
          name: '120mm 3BK18M - HEATFS',
          value: '1300'
        }
      ]
      DDFV.options = types
      console.log(DDFV.selected)
    },
    Calc_Distance: function () {
      this.testvar1 *= 1.34
      console.log(this.distance)
    },
    testfunc1: function () {
      console.log(this.STA1[1])
    }
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
