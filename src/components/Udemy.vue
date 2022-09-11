<template>
  <p>Hello <span class="bg-gray text-blue" v-bind:class="{ large: isLarge, 'text-danger': hasError }">small world</span></p>
</template>

<script setup>
</script>

<script>
import axios from 'axios'
import { debounce } from 'lodash'

export default {
  data() {
    return {
      isLarge: true,
      hasError: true,
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
