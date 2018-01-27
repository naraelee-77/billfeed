<template>
  <div id="app">
    <test :text.sync="text" :moretext.sync="moretext"></test>
    <router-view/>
  </div>
</template>

<script>
import Test from '@/components/Test.vue'

export default {
  name: 'App',
  components: {
    Test
  },
  data: function () {
    return {
      text: 'Data being passed from App to a prop of test',
      moretext: 'woah'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
