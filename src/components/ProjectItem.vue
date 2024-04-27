<script setup>
import {faGithubAlt} from "@fortawesome/free-brands-svg-icons";
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

const props = defineProps({
  title: String,
  description: String,
  link: String,
  technologies: Array
});
</script>

<template>
  <div
      class="group project-item bg-gradient-to-b from-rose-950 via-red-800 to-neutral-4400 shadow-md shadow-rose-950 rounded-lg p-1 flex flex-col transition duration-500 ease-in-out z-10 relative">
    <div class="bg-neutral-950 transition duration-500 group-hover:bg-neutral-600 group-hover:text-black h-full p-6">
      <div class="text-center">
        <h3 class="project-title text-2xl text-center font-semibold mb-4">{{ title }}</h3>
        <a :href="link" target="_blank" class="text-center text-rose-800 hover:text-rose-900 w-full mt-2">
          <span>Source Code </span>
          <FontAwesomeIcon :icon="faGithubAlt"/>
        </a>
      </div>
      <div class="md:min-h-32 lg:min-h-32">
        <p class="project-description group-hover:text-black transition duration-500 text-gray-500 text-lg mb-4">{{ description }}</p>
      </div>
      <h4 class="text-lg text-center font-semibold mb-2">Technologies</h4>
      <ul class="space-y-1 flex flex-col gap-1">
        <li v-for="technology in technologies" :key="technology"
            class="transition duration-500 group-hover:text-black group-hover:bg-neutral-200 text-gray-950 text-sm bg-neutral-800 text-neutral-200 font-bold rounded-full px-3 py-1">{{ technology }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>

</style>