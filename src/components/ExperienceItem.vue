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
  <div class="rounded-lg">
    <div class="border-no-pixel rounded-lg bg-gradient-to-b from-rose-900 via-neutral-900 to-red-900 w-full h-full relative p-1">
      <div class="bg-neutral-950 p-4">
        <h3 class="text-xl font-bold text-gray-200">{{ position }} - {{ company }}</h3>
        <p class="text-gray-300">{{ date }}</p>
        <ul class="list-disc list-inside text-gray-400 mt-4">
          <li v-for="point in points" :key="point">{{ point }}</li>
        </ul>
        <div class="mt-4">
      <span v-for="tech in technologies" :key="tech"
            class="inline-block bg-rose-800 text-gray-200 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded">
        {{ tech }}
      </span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>