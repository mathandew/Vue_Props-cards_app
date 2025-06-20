<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
    <button @click="$emit('remove')">Remove</button>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String
  }
}
</script>

<style scoped>
.card {
  border: 1px solid #ddd;
  padding: 16px;
  margin: 10px;
  border-radius: 8px;
}
</style>
