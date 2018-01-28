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
require('dotenv').config()
var fetch = require('node-fetch')

export default {
  name: 'Card',
  components: {
    Modal
  },
  props: {
    card: {
      title: String,
      intro: String,
      text: String,
      category: String,
      dateIntroduced: String,
      houseOrSenate: String
    }
  },
  data: function () {
    return {
    }
  },

  created: function () {
    this.getBillInfo()
  },

  methods: {
    handleClick: function (event) {
      alert('Hi')
      return 'block'
    },

    getBillInfo: function () {
      var propub = 'https://api.propublica.org/congress/v1/115/bills/hr4881'
      fetch(propub, { headers: {
        'X-API-Key': 'kTURrPH8Awsjo6H8zd7JSEqfyFrxvPO0ubGmbHl6'
      }})
        .then((res) => res.json())
        .then((json) => {
          var results = json.results[0]
          this.card.title = results.short_title
          this.card.intro = results.title
          this.card.text = results.summary
          this.card.category = results.primary_subject
          this.card.houseOrSenate = results.bill_type
          this.card.dateIntroduced = results.introduced_date
        })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
