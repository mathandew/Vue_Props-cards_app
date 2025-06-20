<template>
  <div class="container">
    <h1>📦 Vue Cards App</h1>

    <div class="card-grid">
      <Card
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :description="card.description"
        @remove="removeCard(index)"
      />
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  components: { Card },
  data() {
    return {
      cards: [
        { title: 'Vue 3', description: 'Learn reactivity and components' },
        { title: 'Props & Events', description: 'Pass data & communicate' },
        { title: 'Composition API', description: 'Advanced reusability' }
      ]
    }
  },
  methods: {
    removeCard(index) {
      this.cards.splice(index, 1)
    }
  }
}
</script>

<style>
.container {
  max-width: 900px;
  margin: auto;
  padding: 20px;
  text-align: center;
}

.card-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}
</style>
