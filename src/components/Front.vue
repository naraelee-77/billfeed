<template>
  <div class="front">
    <topbar/>
      <div class="container">
      <img src='../assets/logo.svg'>
      <h1>Bill Feed</h1>
      <p>See what organizations have to say about on-going bills </p>
      </div>
      <hr>
      <div class="content">
        <ul>
          <a href="http://localhost:8080/org_page"><li><img class="enabled" src='../assets/AI.jpg'></li></a>
          <li><img src='../assets/aclu.jpeg'></li>
          <li><img src='../assets/acs.png'></li>
          <li><img src='../assets/as.png'></li>
        </ul>
      </div>

    <bottombar/>
  </div>
</template>

<script>
import Topbar from '@/components/Topbar.vue'
import Bottombar from '@/components/Bottombar.vue'
export default{
  name: 'Front',
  components: {
    Topbar, Bottombar
  }
}
</script>

<style scoped>
h1{
  font-size: 2em;
}

li{
  display:inline-block;
}

li > img{
  width: 8em;
  height: 8em;
  padding: 2em;
}

div > img{
  width: 5em;
  height: 5em;
  padding: 1em;
  float:left;
}
.container{
  padding-left:25em;
  padding-right:25em;
  margin-bottom: 5em;
}
</style>
