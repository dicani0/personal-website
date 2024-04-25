<script setup>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {faPhp, faVuejs, faHtml5, faCss3Alt, faJs, faDocker, faGitAlt, faGithub} from "@fortawesome/free-brands-svg-icons";
import {faDatabase, faCode} from "@fortawesome/free-solid-svg-icons";
import SkillItem from "./SkillItem.vue";
</script>

<template>
  <div class="container mx-auto px-4 min-h-[1000px] h-screen flex flex-col justify-center">
    <section class="py-12 min-h-[800px]">
      <div class="container mx-auto px-4">
        <h2 class="text-4xl font-bold text-center text-gray-800 mb-8">Technical Skills</h2>
        <div class="flex flex-wrap justify-center text-gray-600">

          <SkillItem title="PHP & Laravel" :icon="faPhp" class-string="text-6xl text-blue-500 mb-4"/>
          <SkillItem title="Vue.js" :icon="faVuejs" class-string="text-6xl text-green-500 mb-4"/>
          <SkillItem title="HTML" :icon="faHtml5" class-string="text-6xl text-orange-500 mb-4"/>
          <SkillItem title="CSS" :icon="faCss3Alt" class-string="text-6xl text-blue-400 mb-4"/>
          <SkillItem title="JavaScript" :icon="faJs" class-string="text-6xl text-yellow-400 mb-4"/>
          <SkillItem title="PHPUnit" :icon="faPhp" class-string="text-6xl text-blue-500 mb-4"/>
          <SkillItem title="Docker" :icon="faDocker" class-string="text-6xl text-blue-500 mb-4"/>
          <SkillItem title="RESTful APIs" :icon="faCode" class-string="text-6xl text-red-500 mb-4"/>
          <SkillItem title="Eloquent ORM" :icon="faDatabase" class-string="text-6xl text-blue-900 mb-4"/>
          <SkillItem title="MySQL" :icon="faDatabase" class-string="text-6xl text-blue-500 mb-4"/>
          <SkillItem title="PostgreSQL" :icon="faDatabase" class-string="text-6xl text-blue-700 mb-4"/>
          <SkillItem title="Git" :icon="faGitAlt" class-string="text-6xl text-orange-500 mb-4"/>
          <SkillItem title="GitHub" :icon="faGithub" class-string="text-6xl text-white mb-4"/>

        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>

</style>