<template>
  <div class="grid h-full w-full">
    <div
      class="grid w-full h-full gap-4 py-10"
      :style="{
        gridTemplateColumns: `repeat(${items.length}, minmax(0, ${100 / items.length}%))`,
      }"
    >
      <div
        v-for="(item, index) in items"
        :key="index"
        class="border-2 border-red-300 rounded-3xl text-3xl font-bold flex items-center justify-center p-8 break-words text-center"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { PropType } from "vue";

defineProps({
  items: {
    type: Array as PropType<string[]>,
    required: true,
  },
});
</script>
