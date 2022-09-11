<template>
  <p>Hello <span v-bind:class="largeClass">Vue.js</span></p>
  <p>Hello <span v-bind:class="[largeClass, dangerClass]">Vue.js</span></p>
</template>

<script setup>
</script>

<script>
import axios from 'axios'
import { debounce } from 'lodash'

export default {
  data() {
    return {

      largeClass: 'large',
      dangerClass: 'text-danger',
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
