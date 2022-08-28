<template>
  <p>
    <input type="text" v-model="keyword" />
  </p>
  <p>{{ message }}</p>
  <ul>
    <li v-for="item in items">
      <a v-bind:href="item.url" target="_blank"> {{ item.title }} </a>
      likes: {{ item.likes_count }}
    </li>
  </ul>
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
        // console.log('api response:')
        // console.log(response)
        vm.items = response.data
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
