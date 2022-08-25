<template>
  <p>{{ message }}</p>
  <input type="text" v-model="message" />aa


</template>

<script>
export default {
  data() {
    return { message: "Helloo" }
  },
  watch: {
    message: function(newValue, oldValue) {
      console.log('New:', newValue, 'Old:', oldValue)

    }
  }
}
</script>

<style scoped>
</style>
