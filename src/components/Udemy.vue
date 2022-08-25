<template>
  <p><input type="text" v-model="km" />km</p>
  <p><input type="text" v-model="m" />m</p>
</template>

<script>
export default {
  data() {
    return {
      km: 0,
      m: 0
    }
  },
  watch: {
    km: function(value) {
      console.log('km:', value)
      this.m = value * 1000
    },
    m: function(value) {
      console.log('m:', value)
      this.km = value / 1000
    },
  }
}
</script>

<style scoped>
</style>
