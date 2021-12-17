<template>
  <div>

      <h2 :id="headingId">heading</h2>
      <button :disabled="isDisabled">bind</button>
      <h2 class="underline">Underline text</h2>
      <h2 class="underline" :class="status">status</h2>
      <h2 :class="isPromoted && 'promoted'">promoted movie</h2>
      <h2 :class="isSoldOut ? 'sold-out' : 'new'">is the movie sold out?</h2>
      <h2 :class="['new', 'promoted']">newly promoted movies</h2>
      <h2 :class="[isSoldOut ? 'sold-out' : 'new', isPromoted && 'promoted']">arry conditionalmovies</h2>
      <h2 :class="{
        promoted: isPromoted,
        new: !isSoldOut,
        'sold-out': isSoldOut

      }">object conditional movie</h2>

      <h2 :style="{color: highlightColor, 'font-size': headerSize + 'px', padding: '20px'}">inline stile</h2>
      <h2 :style="headerStyleObject">this is style object</h2>

      <h2 :style="[baseStyleObject,successStyleObject]">Success style</h2>
      <h2 :style="[baseStyleObject,dengerStyleObject]">denger style</h2>
  </div>
</template>

<script>
export default {
  name: 'App',

  data(){
    return {

      headingId: 'beka',
      isDisabled: true,
      status: 'success',
      isPromoted: true,
      isSoldOut: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'

      },
      baseStyleObject:{
        fontSize: '50px',
        padding: '20px'
      },
        successStyleObject:{
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green'

      },        
      dengerStyleObject:{
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid red'

      },
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

.underline{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}

.new{
  color: olivedrab;
}
.sold-out{
  color: red;
}
</style>
