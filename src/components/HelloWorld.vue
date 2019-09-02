<template>
  <div class="hello">
    <h1 class="animated rollIn bounce delay-2s">{{ msg }}</h1>
    <div class="square animated flipOutY"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
.square {
  background-color: blue;
  height: 200px;
  width: 200px;
}
</style>
