<template>
  <div class="card">
    <modal :title.sync="card.title"
           :text.sync="card.text"
           />
    <button v-on:click="handleClick">
      <div class="content">
        <h2> {{card.title}} </h2>
        <hr>
        <p> {{card.intro}} </p>
      </div>
    </button>
  </div>
</template>

<script>
import Modal from '@/components/Modal.vue'

export default {
  name: 'Card',
  components: {
    Modal
  },
  props: {
    card: {
      title: String,
      intro: String,
      text: String
    }
  },
  data: function () {
    return {
    }
  },
  methods: {
    handleClick: function (event) {
      event.target.previousElementSibling.style.display = 'block'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  margin: 1em;
}
button{
  text-align: left;
  width: 50em;
  border-left: 6px solid blue;
  border-bottom:none;
  border-right:none;
  background-color:white;
  transition: .15s;
  border-radius: 5px;
}

button:hover{
  background-color: #f0f0f0;
  border-left: 9px solid red;
}

</style>
