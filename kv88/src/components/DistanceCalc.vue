<template>
    <div class="DistanceCalcDiv">
        <div class="roundType" id="DCIs">
            <h2>Select Round (mm)(name)(type)
            </h2>
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
            <div id="inputL">
              <button @click="CalculatePen">Calculate</button>
              <select v-model="selected" class="form-control sl">
              <option v-for="option in options" :value="option.value" :key="option.value">{{ option.name }}</option>
              </select>
            </div>
        </div>
        <div class="distanceInput" id="DCIs">
          <h2>Distance the Round Traveled (meters)</h2>
          <div id="inputL">
            <input type="number" id="IANi" name="IANn" min='-90' max='90' v-model="angle"><br>
          </div>
        </div>
        <div class="penAtDisOutput" id="DCIs">
          <h2>{{PEN}}mm</h2>
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
      angle: 1,
      options: ['152mm G-530 - The Anti-Concrete'],
      selected: '400',
      PEN: 0
    }
  },
  methods: {
    dropDown: function () {
      console.log(this.angle)
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
    CalculatePen: function () {
      console.log(this.selected * 3)
      this.PEN = this.selected * this.angle
    }
  },
  created: function () {
    this.dropDown()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#DCIs {
  background-color: gray;
  Margin: 5% 10% 5% 10%;
  padding:2% 2% 2% 2% ;
}

.demoDiv {
  margin:2% 5% 2% 5% ;
  justify-content: center;
  background-color: black;
}

/* .angleInput{
  margin:2% 5% 2% 5% ;
  justify-content: center;
  background-color: gray;
} */

#inputL {
  background-color: lightgray;
  Margin: 5% 10% 5% 10%;
  padding:2% 2% 2% 2% ;
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
