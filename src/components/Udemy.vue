<template>
</template>

<script setup>
</script>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      items: null,
      keyword: '',
      message: ''
    }
  },
  watch: {
  },
  mounted: function() {
    this.keyword = 'JavaScript'
    this.getAnswer()
  },
  methods: {
    getAnswer: function() {
      if (this.keyword === '') {
        console.log('karamoji')
        this.items = null
        return
      }
      this.message = 'Loading..'
      // thisをローカル変数に入れておく
      const vm = this

      const params = { page: 1, per_page: 10, query: this.keyword }
      axios.get('https://qiita.com/api/v2/items', { params })
      .then(function(response){
        console.log('api response:')
        console.log(response)
      })
      .catch(function(error){
        console.log(error)
        vm.message = 'Error:' + error
      })
      .finally(function() {
        console.log("finally.")
        vm.message = ""
      })

    }
  }
}
</script>

<style scoped>
</style>
