<script setup>
import HomeSection from "./components/HomeSection.vue";
import Navbar from "./components/Navbar.vue";
import AboutSection from "./components/AboutSection.vue";
import SkillsSection from "./components/SkillsSection.vue";
import ExperienceSection from "./components/ExperienceSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import ContactSection from "./components/ContactSection.vue";
</script>

<template>
<!--  <Navbar/>-->
  <main class="bg-neutral-950">
    <div id="home">
      <HomeSection/>
    </div>
    <div id="about">
      <AboutSection/>
    </div>
    <div id="skills">
      <SkillsSection/>
    </div>
    <div id="experience">
      <ExperienceSection/>
    </div>
    <div id="projects">
      <ProjectsSection/>
    </div>
    <div id="contact">
      <ContactSection/>
    </div>
  </main>
</template>

<style scoped>

</style>
