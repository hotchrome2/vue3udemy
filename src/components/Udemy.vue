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
      ],
      index: 0,
      count: 0,
    }
  },
  watch: {
    colors: {
      handler: function(newValue, oldValue) {
        // 本当に新旧の値が違う時のみここに来る
        this.count++;
        console.log('Updated. count:', this.count)
      },
      deep: true
    }
  },
  methods: {
    onClick: function(event) {
      this.index++;
      if (this.index >= 3) {
        this.index = 0;
      }
      console.log('index:', this.index)
      this.colors[this.index].name = 'White'
    }
  }
}
</script>

<style scoped>
</style>
