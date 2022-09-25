<template>
  <p>sec11 85 use event handler</p>
  <p >
    counter: {{ counter }}
  </p>
  <button v-on:click="counter++">Click here</button>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      counter: 0,
    }
  },
}
</script>

<style scoped>
  .large {
    font-size: 30px;
  }
  .text-danger {
    color: red;
  }
  .bg-gray {
    background-color: gray;
  }
  .text-blue {
    color: blue;
  }
</style>
