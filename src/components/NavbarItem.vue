<script setup>
const props = defineProps({
  type: String,
  title: String,
  section: String,
});
</script>

<template>
  <li>
    <a :href="props.section" class="flex gap-2">
      <vue-feather :type="props.type"></vue-feather>
      <span>{{ props.title }}</span>
    </a>
  </li>
</template>
