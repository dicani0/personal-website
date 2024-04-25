<script setup>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {faPhp, faVuejs, faHtml5, faCss3Alt, faJs, faDocker, faGitAlt, faGithub} from "@fortawesome/free-brands-svg-icons";
import {faDatabase, faCode} from "@fortawesome/free-solid-svg-icons";

defineProps({
  title: String,
  icon: Object,
  classString: String,
});
</script>

<template>
  <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
    <div class="text-center">
      <div class="text-2xl text-gray-800 font-semibold mb-2">{{ title }}</div>
      <FontAwesomeIcon :icon="icon" :class="classString"/>
    </div>
  </div>
</template>

<style scoped>

</style>