<template>
  <div>
    <h2 v-if="num===0">The number is zero {{num}}</h2>
    <h2 v-else-if="num<0">The number is Negative {{num}}</h2>
    <h2 v-else-if="num>0">The number is possitive {{num}}</h2>
    <h2 v-else>not a number {{num}}</h2>

    <template v-if="display">
      <h2>beka</h2>
      <h2>vue</h2>
      <h2>toturials</h2>
    </template>


  </div>
</template>

<script>
export default {
  name: 'App',

  data(){
    return {
      num: 'hi',
      display: true
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
