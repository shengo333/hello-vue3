<template>
  <div>
    <h2 v-for="(name, index) in names" :key="index">{{index}} {{name}}</h2>
    <h2 v-for="(fullName, index) in fullNames" :key="index">{{fullName.first}} {{fullName.last}}</h2>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{actor.name}}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3> 

    </div>

    <h2 v-for="(value, key, index) in myInfo" :key="value"> {{index}} {{key}} {{value}}</h2>

    <div v-for="name in names" :key="name">
      <h2>{{name}}</h2>
      <hr>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',

  data(){
    return {
      names: ['bruce', 'joker', 'betman'],
      fullNames:[
        {first: 'bruce', last: 'wayne'},
        {first: 'john', last: 'frusciante'},
        {first: 'jango', last: 'unchained'}
      ],      
      actors:[
        {
          name: 'Christian bale', 
          movies: ['Betman', 'Prestige']
        },
        {
          name: 'Di caprio', 
          movies: ['Titanic', 'inception']
        },
      ],
      myInfo:{
        name: 'wishvas',
        channel: 'codevolution',
        course: 'vue 3'
      }
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
