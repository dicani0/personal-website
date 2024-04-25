<script setup>
defineProps({
  position: String,
  company: String,
  date: String,
  points: Array,
  technologies: Array
})
</script>

<template>
  <div class="bg-neutral-900 p-6 rounded-lg shadow-xl relative ring ring-rose-900 p-16 shadow-rose-950">
    <h3 class="text-xl font-bold text-gray-300">{{ position }} - {{ company }}</h3>
    <p class="text-gray-400">{{ date }}</p>
    <ul class="list-disc list-inside text-gray-500 mt-4">
      <li v-for="point in points" :key="point">{{ point }}</li>
    </ul>
    <div class="mt-4">
      <span v-for="tech in technologies" :key="tech" class="inline-block bg-rose-800 text-gray-200 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded">
        {{ tech }}
      </span>
    </div>
  </div>
</template>

<style scoped>

</style>