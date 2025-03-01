<template>
  <div class="box-list">
    <div v-for="(challenge, index) in challenges" :key="index" class="box-item">
      <div class="box-title">{{ challenge.title }}</div>
      <div v-if="challenge.content" class="box-content">
        {{ challenge.content }}
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  challenges: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped>
.box-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}

.box-item {
  padding: 1.5rem;
  border-radius: 1.5rem;
  border: 2px solid #fca5a5;
  text-align: center;
  display: flex;
  flex-direction: column;
}

.box-title {
  font-size: 1.25rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.box-content {
  font-size: 0.875rem;
  color: #666;
}
</style>
