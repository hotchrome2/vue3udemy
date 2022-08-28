<template>
  <ul>
    <li v-for="color in colors">
      {{ color.name}}
    </li>
  </ul>
  <button v-on:click="onClick">Click here</button>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      colors : [
        { name: 'Red'},
        { name: 'Green'},
        { name: 'Blue'},
      ]
    }
  },
  watch: {
    colors: {
      handler: function(newValue, oldValue) {
        console.log('Updated.')
      },
      deep: true
    }
  },
  methods: {
    onClick: function(event) {
      this.colors[1].name = 'White'
    }
  }
}
</script>

<style scoped>
</style>
