<template>
  <p>sec11 86 use event handler method</p>
  <p >
    counter: {{ counter }}
  </p>
  <button v-on:click="clickHandler">Click Here.</button>
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
  methods: {
    clickHandler: function() {
      this.counter++;
    }
  }
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
