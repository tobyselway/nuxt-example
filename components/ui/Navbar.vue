<script setup lang="ts">
interface Item {
  title: string
  to: string
};

defineProps({
  title: String,
  items: { type: Array<Item>, required: true },
});
</script>

<template>
  <div class="flex items-center w-full h-16 gap-6 p-4 text-gray-400 bg-gray-900">
    <h1 class="mr-3 text-3xl font-bold tracking-tighter text-gray-200">
      {{ title }}
    </h1>
    <NuxtLink
      v-for="item in items"
      :key="item.to"
      :to="item.to"
      class="text-lg font-semibold tracking-tight hover:text-gray-300"
      exact-active-class="text-gray-100"
    >
      {{ item.title }}
    </NuxtLink>
  </div>
</template>
