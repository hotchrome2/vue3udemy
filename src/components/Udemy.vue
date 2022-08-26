<template>
  <p>first:<input type="text" v-model="first" /></p>
  <p>last:<input type="text" v-model="last" /></p>
  <p>Full Name: {{ fullName }}</p>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      first: "",
      last: "",
      // fullName: ""
    }
  },
  computed: {
    fullName: function() {
      return this.first + ',' + this.last
    }
  }
  // watch: {
  //   first: function(value) {
  //     this.fullName = value + ' ' + this.last
  //     console.log('first:', value)
  //   },
  //   last: function(value) {
  //     this.fullName = this.first + ' ' + value
  //     console.log('last:', value)
  //   },
  // }
}
</script>

<style scoped>
</style>
