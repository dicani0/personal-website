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
  <div class="px-4 mb-8">
    <div class="text-center relative bg-neutral-950">
      <div class="text-2xl text-gray-500 font-semibold mb-2">{{ title }}</div>
      <FontAwesomeIcon :icon="icon" :class="classString"/>
    </div>
  </div>
</template>

<style scoped>

</style>