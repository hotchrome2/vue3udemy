<template>
  <p>sec10 80</p>
  <p v-if="toggle">Yes</p>
  <p v-else>No</p>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      toggle: false,
    }
  },
  watch: {
  },
  mounted: function() {
  },
  methods: {
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
