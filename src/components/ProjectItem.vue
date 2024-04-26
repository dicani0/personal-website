<script setup>
import {faGithubAlt} from "@fortawesome/free-brands-svg-icons";
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

const props = defineProps({
  title: String,
  description: String,
  link: String
});
</script>

<template>
  <div class="project-item bg-neutral-950 shadow-md shadow-rose-950 rounded-lg p-6 flex flex-col">
    <h3 class="project-title text-xl text-center font-bold mb-2">{{ title }}</h3>
    <p class="project-description text-gray-700 mb-2">{{ description }}</p>
    <a :href="link" target="_blank" class="text-center text-rose-800 hover:text-rose-900 w-full">
      <span>Source Code </span>
      <FontAwesomeIcon :icon="faGithubAlt"/>
    </a>
  </div>
</template>

<style scoped>

</style>