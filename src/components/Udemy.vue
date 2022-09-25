<template>
  <p>sec10 82 use v-show</p>
  <p v-show="toggle">
    Hello
  </p>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      toggle: true,
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
