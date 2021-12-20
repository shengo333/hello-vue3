<template>
  
  <div>
    <h2>{{name}}</h2>
    <div>
      <button @click="changeName($event), incriment(1, $event)">change name</button>
    </div>
    <h2>{{count}}</h2>
    <div>
      <button @click="incriment(10, $event)">incriment 10</button>
      <button @click="incriment(5)">incriment 5</button>

      <button @click="decriment(10)">decriment 10 </button>
      <button @click="decriment(5)">decriment 5</button>
    </div>
  </div>
  
</template>

<script>

export default {
  name: "App",
  data() {
    return{
      name: 'wishvas',
      count: 0,
      num: 5
    }
  },
  methods:{
    incriment(num){
      this.count +=num
      console.log('Event',event)
    },    
    decriment(num){
      this.count -=num
    },
    changeName(){
      this.name = 'shengo'
      console.log('Event',event)
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
