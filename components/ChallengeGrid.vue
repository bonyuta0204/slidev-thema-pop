<!-- components/ChallengeGrid.vue -->
<template>
  <div class="challenge-grid">
    <div v-for="(challenge, index) in challenges" :key="index" class="challenge-box">
      <div class="challenge-title">{{ challenge.title }}</div>
      <div v-if="challenge.content" class="challenge-content">{{ challenge.content }}</div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  challenges: {
    type: Array,
    required: true
  }
});
</script>

<style scoped>
.challenge-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  margin-top: 2.5rem;
}

.challenge-box {
  padding: 1.5rem;
  border-radius: 1.5rem;
  border: 2px solid #FCA5A5;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.challenge-title {
  font-size: 1.5rem;
  font-weight: bold;
}

.challenge-content {
  margin-top: 1rem;
}
</style>
