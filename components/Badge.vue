<template>
  <div class="badge">
    <slot></slot>
  </div>
</template>

<style scoped>
.badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background-color: #f87171;
  color: white;
  padding: 0.25rem 1rem;
  border-radius: 0.375rem;
}
</style>
