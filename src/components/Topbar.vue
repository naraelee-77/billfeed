<template>
  <div class="topbar">
    <i class="fa fa-file-text"/>
    <h3><a href="/">Bill Feed</a></h3>
  </div>
</template>

<script>
import 'font-awesome/css/font-awesome.css'
export default {
  name: 'Topbar'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.topbar{
    text-align: left;
    background-color: #bbbbbb;
    height: 2em;
    padding-top:.5em;
}

i {
   display: inline;
   margin-left: 1em;
   margin-right: 1em;
}
h3 {
   display: inline
}
a{
    text-decoration: none;
    color:inherit;
}
</style>
