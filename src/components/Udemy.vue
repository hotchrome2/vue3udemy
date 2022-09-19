<template>
  <p>sec10 81</p>
  <p v-if="color === 'red'">
    Stop
  </p>
  <p v-else-if="color === 'yellow'">
    Caution
  </p>
  <p v-else-if="color === 'blue'">
    Go
  </p>
  <p v-else>Not red/yellow/blue</p>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      color: 'yellow',
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
