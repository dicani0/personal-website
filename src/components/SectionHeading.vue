<script setup>
defineProps({
  text: String
});
</script>

<template>
  <h2 class="text-4xl font-bold text-center text-gray-400 mb-8">
    <slot></slot>
  </h2>
</template>

<style scoped>

</style>