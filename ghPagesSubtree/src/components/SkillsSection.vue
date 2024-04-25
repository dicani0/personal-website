<script setup>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {faPhp, faVuejs, faHtml5, faCss3Alt, faJs, faDocker, faGitAlt, faGithub} from "@fortawesome/free-brands-svg-icons";
import {faDatabase, faCode} from "@fortawesome/free-solid-svg-icons";
</script>

<template>
  <div class="container mx-auto px-4 min-h-[1000px] h-screen flex flex-col justify-center">
    <section class="py-12 min-h-[800px]">
      <div class="container mx-auto px-4">
        <h2 class="text-4xl font-bold text-center text-gray-800 mb-8">Technical Skills</h2>
        <div class="flex flex-wrap justify-center text-gray-600">

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">PHP & Laravel</div>
              <FontAwesomeIcon :icon="faPhp" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">Vue.js</div>
              <FontAwesomeIcon :icon="faVuejs" class="text-6xl text-green-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">HTML</div>
              <FontAwesomeIcon :icon="faHtml5" class="text-6xl text-orange-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">CSS</div>
              <FontAwesomeIcon :icon="faCss3Alt" class="text-6xl text-blue-400 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">JavaScript</div>
              <FontAwesomeIcon :icon="faJs" class="text-6xl text-yellow-400 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">PHPUnit</div>
              <FontAwesomeIcon :icon="faPhp" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">Docker</div>
              <FontAwesomeIcon :icon="faDocker" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">RESTful APIs</div>
              <FontAwesomeIcon :icon="faCode" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">Eloquent ORM</div>
              <FontAwesomeIcon :icon="faDatabase" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">MySQL</div>
              <FontAwesomeIcon :icon="faDatabase" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">PostgreSQL</div>
              <FontAwesomeIcon :icon="faDatabase" class="text-6xl text-blue-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">Git</div>
              <FontAwesomeIcon :icon="faGitAlt" class="text-6xl text-orange-500 mb-4"/>
            </div>
          </div>

          <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 px-4 mb-8">
            <div class="text-center">
              <div class="text-2xl text-gray-800 font-semibold mb-2">GitHub</div>
              <FontAwesomeIcon :icon="faGithub" class="text-6xl text-black mb-4"/>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>

</style>