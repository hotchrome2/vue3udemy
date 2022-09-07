<template>
  <p>Hello <span v-bind:class="{large: isLarge}">small world</span></p>
  <p>Hello <span :class="{large: isLarge}">small World!</span></p>
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
</style>
