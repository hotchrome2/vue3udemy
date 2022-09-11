<template>
  <p>Hello sec9-78,<span v-bind:style="styleObject">Vue.js</span></p>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      styleObject: {
        color: 'pink',
        fontSize: '28px',
      }
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
