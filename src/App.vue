<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Patua+One');
#app {
  /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
  font-family: Patua One;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  animation-name: fadein;
  animation-duration: 1s;
}

@keyframes fadein{
  from{opacity: 0;}
  to {opacity: 1;}
}
</style>
