<!-- components/MenuList.vue -->
<template>
  <div class="flex flex-col space-y-4 h-100 justify-center flex-1">
    <div
      v-for="(item, index) in items"
      :key="index"
      :class="[
        'flex flex-1 items-center p-2 px-8 rounded-full transition-colors duration-300 max-h-15',
        activeIndex === index
          ? 'bg-blue-400 text-white'
          : 'bg-gray-100 text-gray-500',
      ]"
    >
      <div class="text-xl font-bold">{{ item }}</div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  items: {
    type: Array,
    required: true,
  },
  activeIndex: {
    type: Number,
    required: false,
  },
});
</script>
