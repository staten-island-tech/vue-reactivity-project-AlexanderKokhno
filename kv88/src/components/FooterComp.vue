<template>
  <div class="FooterCompDiv">
    <h1>Lorem ipsum dolor, sit amet consectetur tates repudiandae maiores sequi aliquam accusamus cu</h1>
  </div>
</template>

<script>
export default {
  name: 'FooterComp',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.FooterCompDiv {
  padding:2% 2% 2% 2% ;
  position:relative;
  bottom: 0;
  width: 100%;
  background-color: black;
  height: auto;
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
