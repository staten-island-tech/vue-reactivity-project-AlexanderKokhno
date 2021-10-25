<template>
    <div class="DistanceCalcDiv">
        <div class="ShellType">
            <p>Select Measurement Unit(Of Coffee Drank)
            </p>
            <form>
                <select name="ShellDPn" id="ShellDPn">
                    <option value="KLm" id="KL_MU" selected="selected"></option>
                    <option value="OBm" id="OB_MU"></option>
                    <option value="MLm" id="ML_MU"></option>
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
      kv2_ac: 'G-530 (AC) - The Anti-Concrete',
      STA1: ['152mm G-530 (AC) - The Anti-Concrete', '88mm', '128mm'],
      document.getElementById("KL_MU").innerHTML = STA1[0],
      document.getElementById("OB_MU").innerHTML = STA1[1],
      document.getElementById("ML_MU").innerHTML = STA1[2],
      gei_kv2_ac: document.getElementById('hello').outerHTML
    }
  },
  methods: {
    Calc_Distance: function () {
      this.distance *= 1.34
      console.log(this.distance)
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
