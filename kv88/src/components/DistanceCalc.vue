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
            <input type="number" id="IANi" name="IANn" min='0' v-model="distance"><br>
          </div>
        </div>
        <div class="penAtDisOutput" id="DCIs">
          <h2>Round can penetrate {{PEN}}mm of unsloped armour.</h2>
        </div>
        <div class = "RoundInfo" id="DCIs">
          <h2>Information</h2>
          <div class="roundType">
          </div>
            <div id="infoGifDiv">
            <div v-if="selected === '530'" class="DDKV" id="INFODIV">
              <img alt="Vue logo" class="imKV" id="INFOPIC" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
            <div class="DDKT" v-else-if="selected === '1000'" id="INFODIV">
              <img alt="Vue logo" class="imKT" id="INFOPIC"  Src="https://i.pinimg.com/originals/ea/97/89/ea978942986c010e36bb11aa7e9bec14.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
            <div class="DDMAUS" id="INFODIV" v-else-if="selected === '1230'">
              <img alt="Vue logo" class="imMAUS" id="INFOPIC"  Src="https://media1.giphy.com/media/Y2Pe0rZqu6NaU2Iec1/giphy.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
            <div v-if="selected === '960'" class="DDUST34" id="INFODIV">
              <img alt="Vue logo" class="imUST34" id="INFOPIC" Src="https://thumbs.gfycat.com/ImmaterialAbandonedHermitcrab-max-1mb.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
            <div v-if="selected === '1660'" class="DDLEO" id="INFODIV">
              <img alt="Vue logo" class="imLEO" id="INFOPIC"  Src="https://thumbs.gfycat.com/PlayfulConfusedArmadillo-max-1mb.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
            <div v-if="selected === '950'" class="DDT80" id="INFODIV">
              <img alt="Vue logo" class="imT80" id="INFOPIC" Src="https://78.media.tumblr.com/4c7fbba51be362743c5c44b77109ec0f/tumblr_nl7wsbs2Ho1t382eqo4_500.gif">
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta architecto et, distinctio adipisci ducimus delectus explicabo non minus nisi aliquid tenetur. Incidunt deleniti provident cumque. Architecto nisi quia minus nemo!
            </p>
            </div>
          </div>
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
      distance: 1,
      angle: 1,
      options: ['128mm 12,8/8,8 Pzgr.TS - APCBC'],
      selected: '1230',
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
          value: '530'
        },
        {
          name: '88mm (PzGr 39/43) - APCBC',
          value: '1000'
        },
        {
          name: '128mm 12,8/8,8 Pzgr.TS - APCBC',
          value: '1230'
        },
        {
          name: '120mm T14E3 - APCBC',
          value: '960'
        },
        {
          name: '120mm DM43 - APFSDS',
          value: '1660'
        },
        {
          name: '120mm 3BK18M - HEATFS',
          value: '950'
        }
        {
          name:'76.2mm Tea - APDS'
          value:'428261482'


        }
      ]
      DDFV.options = types
      console.log(DDFV.selected)
    },
    CalculatePen: function () {
      if (this.selected === '530') {
        this.PEN = (((this.distance * this.distance) * 61) / 73010000) - ((92511 * this.distance) / 7301000) + (1389039 / 14602)
      } else if (this.selected === '1000') {
        this.PEN = (((this.distance * this.distance) * 8) / 4563125) - ((57507 * this.distance) / 1825250) + (1732636 / 7301)
      } else if (this.selected === '1230') {
        this.PEN = (((this.distance * this.distance) * 293) / 73010000) - ((372543 * this.distance) / 7301000) + (4563269 / 14602)
      } else if (this.selected === '960') {
        this.PEN = (((this.distance * this.distance) * 69) / 36505000) - ((152519 * this.distance) / 3650500) + (2069232 / 7301)
      } else if (this.selected === '1660') {
        this.PEN = (((this.distance * this.distance) * 57) / 36505000) - ((62507 * this.distance) / 3650500) + (3914585 / 7301)
      } else if (this.selected === '950') {
        this.PEN = (950)
      } else {
        alert('Something went wrong. Either the Round doesnt have a parabula equation or there is a code error')
      }
    }
    // CalculatePenKV: function () {
    //   console.log(this.selected * 3)
    //   // this.PEN = this.selected * this.angle
    //   this.PEN = (((this.distance * this.distance) * 61) / 73010000) - ((92511 * this.distance) / 7301000) + (1389039 / 14602)
    // }
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

.InfoDiv {
  background-color: gray;
  Margin: 5% 10% 5% 10%;
  padding:2% 2% 2% 2% ;
}

#INFODIV {
  margin:2% 5% 2% 5% ;
  justify-content: center;
  padding:2% 5% 2% 5% ;
  height: auto;
  background-color: lightgray;
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
