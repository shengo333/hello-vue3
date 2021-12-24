<template>
  <div>
      <h2>Volume tracker(0-20)</h2>
      <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase volume</button>
      <button @click="volume -= 2">Decrease volume</button>
    </div>
    <input type="text" v-model="movie">
    <input type="text" v-model="movieInfo.title">
    <input type="text" v-model="movieInfo.actor">
    <div>
      <button @click="movieList =movieList.concat (['wonderwomen'])">add movie</button>
    </div>
  </div>
</template>

<script>

export default {
  name: "App",
  data() {
    return{
      volume: 0,
      movie: 'Batman',
      movieInfo:{
        title: '',
        actor: '',
      },
      movieList:['Batman','Superman']
    }
  },
  methods:{},
  computed:{},
  watch:{
    volume (newValue, oldValue){
      if(newValue >oldValue && newValue ===16){
        alert('this is dengerouse for your ears')
      }
    },
    movie: {
      handler(newValue){
      console.log(`we are consoling new value for movie which is: ${newValue}`)
      },
    immediate: true,
    },
    movieInfo: {
      handler(newValue){
      console.log(`we are consoling new value for movie info ${newValue.title} and ${newValue.actor}`)
      },
    deep: true,
    },
    movieList: {
      handler(newValue){
        console.log(`updatedList ${newValue}`)
      },
      //deep: true
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

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
  
}

input label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'],
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.32857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  display: inline-block;
}


form{
  padding: 30px;
}


</style>
