<template>
  <p>Hello <span v-bind:style="{ color: color, fontSize: fontSize + 'px'}">Vue.js</span></p>
  <p>Hello <span v-bind:style="{ color: color, 'font-size': fontSize + 'px'}">Vue.js</span></p>
</template>

<script setup>
</script>

<script>
import axios from 'axios'
import { debounce } from 'lodash'

export default {
  data() {
    return {
      color: 'blue',
      fontSize: 36,
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
