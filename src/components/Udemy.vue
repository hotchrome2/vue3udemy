<template>
  <p>Hello <span v-bind:class="isLarge ? largeClass: ''">Vuejs</span></p>
  <p>Hello <span v-bind:class="[isLarge ? largeClass: '', dangerClass]">Vuejs</span></p>
</template>

<script setup>
</script>

<script>
import axios from 'axios'
import { debounce } from 'lodash'

export default {
  data() {
    return {
      largeClass: {
        large: true,
        'bg-gray': true
      },
      dangerClass: {
        'text-danger': true,
      },
      isLarge: true,
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
