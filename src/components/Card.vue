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
  text-align: left;
  background-color: #f9f9f9;
  transition: box-shadow 0.2s;
}

.card:hover {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

button {
  margin-top: 10px;
  padding: 6px 12px;
  background: #ff4d4d;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
