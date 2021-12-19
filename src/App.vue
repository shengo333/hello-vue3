<template>
  
  <div>
    {{2+5+6}}
    {{5+6+7}}
    <h2> add method is here: {{add(4,6,15)}}</h2>
    <h2> add method is here: {{add(4,20,15)}}</h2>
    <h2>this is multiply method with data: {{multiply(basevalue)}}</h2>
  </div>
      
  
</template>

<script>

export default {
  name: "App",
  data() {
    return{
      baseMultiplier: 5,
      basevalue: 12
    }
  },
  methods:{
    add( a,b,c){
      return a+b+c
    },
    multiply(num){
      return num * this.baseMultiplier
    }
  }
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
