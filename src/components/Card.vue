<template>
  <div class="card">
    <modal/>
    <button v-on:click="handleClick">
      <div class="content">
        <h2> {{card.title}} </h2>
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
      alert('Hi')
      return 'block'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
