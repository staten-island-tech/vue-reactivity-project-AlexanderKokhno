<template>
    <div class="DistanceCalcDiv">
        <div class="ShellType">
            <p>Select Measurement Unit(Of Coffee Drank)
            </p>
            <form>
                <select name="ShellDPn" id="ShellDPn" v-on:change="Calc_Distance" >
                    <option id="PLCH" selected>Select Shell Type Here</option>
                    <option value="KLm" id="KV_AC" v-on:click="Test1">{{STA1[0]}}</option>
                    <option value="OBm" id="OB_MU">{{STA1[1]}}</option>
                    <option value="MLm" id="ML_MU">{{STA1[2]}}</option>
                    <option value="MLm2" id="ML_MU2">{{STA1[3]}}</option>
                    <option value="MLm3" id="ML_MU3">{{STA1[4]}}</option>
                    <option value="MLm4" id="ML_MU4">{{STA1[5]}}</option>
                </select>
            </form>
            <button v-on:click="Calc_Distance" id="Calc_Btn">Calculate</button>
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
      distance: 7,
      STA1: ['152mm G-530 - The Anti-Concrete', '88mm (PzGr 39/43) - APCBC', '128mm 12,8/8,8 Pzgr.TS - APCBC', '120mm T14E3 - APCBC', '120mm DM43 - APFSDS', '120mm 3BK18M - HEATFS']
      // gei_kv2_ac: document.getElementById('KV_AC')
    }
  },
  methods: {
    Calc_Distance: function () {
      this.distance *= 1.34
      console.log(this.distance)
    },
    Test1: function () {
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
