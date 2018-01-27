<template>
  <div class="home">
    <topbar/>
    <h1>Bill Feed</h1>
    See what organizations have to say about on-going bills
    <div class="card-view">
      <card :card.sync="Card1"/>
      <card :card.sync="Card2"/>
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
import Topbar from '@/components/Topbar.vue'
export default {
  name: 'Home',
  components: {
    Card, Topbar
  },
  data: function () {
    return {
      Card1: {
        title: 'Amazing Bill',
        intro: 'Introduction To this bill'
      },
      Card2: {
        title: 'Not a cool bill',
        intro: 'text here lol'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
