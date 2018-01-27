<template>
  <div class="bottombar">
    <div class="spacer"></div>
    <div class="content">
      Bill Feed © 2018
    </div>
  </div>
</template>

<script>
import 'font-awesome/css/font-awesome.css'
export default {
  name: 'bottombar'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.spacer{
  height:2em;
}
.content{
  position:fixed;
  bottom:0;
  left:0;
  width:100%;
  padding:1em;
}
</style>
