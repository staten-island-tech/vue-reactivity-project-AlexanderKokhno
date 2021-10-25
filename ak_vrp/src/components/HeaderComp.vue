<template>
  <div class="HeaderCompDiv">
    <img alt="Vue logo" Src="https://c.tenor.com/Swr_VRFiVvYAAAAC/tanks-cartoon.gif">
    <h1>Trajectory Calculator of Diffrent Tank Shell Types</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.HeaderCompDiv {
  background-color: gray;
  Margin: 5% 10% 0% 10%;
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
