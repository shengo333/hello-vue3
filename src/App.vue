<template>
  <div>
      <div>
        {{greet}} {{name}}
      </div>
      <div v-html="channel">
      </div>
      <div v-html="hack"></div>
  </div>
</template>

<script>
export default {
  name: 'App',

  data(){
    return {
      greet: 'hello',
      name: "shengo",
      channel: '<b>Codevolution</b>',
      hack: '<a href="#" onClick=alert("hacked")>win a prize!<a/>',
    };
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
