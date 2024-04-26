<script setup>
import SectionHeading from "./SectionHeading.vue";
import ProjectItem from "./ProjectItem.vue";

const projects = [
  {
    title: "Game Manager",
    description: "This is a short description of Project 1.",
    link: "https://github.com/dicani0/game-manager",
    technologies: [
      {
        name: "Laravel",
        icon: "laravel"
      },
      {
        name: "Vue.js",
        icon: "vuejs"
      },
      {
        name: "Tailwind CSS",
        icon: "tailwindcss"
      }
    ]
  },
  {
    title: "Laravel LMS (WIP)",
    description: "This is a short description of Project 2.",
    link: "https://github.com/dicani0/laravel-lms",
    technologies: [
      {
        name: "Laravel",
        icon: "laravel"
      },
      {
        name: "Vue.js",
        icon: "vuejs"
      },
      {
        name: "Tailwind CSS",
        icon: "tailwindcss"
      }
    ]
  },
  {
    title: "Task Manager (WIP)",
    description: "This is a short description of Project 3.",
    link: "https://github.com/dicani0/task-manager-backend",
    technologies: []
  },
  {
    title: "Portfolio Website",
    description: "This is a short description of Project 4.",
    link: "https://dicani0.github.io/personal-website/",
    technologies: [
      {
        name: "Vue.js",
        icon: "vuejs"
      },
      {
        name: "Tailwind CSS",
        icon: "tailwindcss"
      }
    ]
  }
];
</script>

<template>
  <div class="container mx-auto px-4 min-h-dvh flex flex-col justify-center">
    <section class="py-12">
      <div class="container mx-auto px-4">
        <SectionHeading>Projects</SectionHeading>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 lg:gap-4">
          <ProjectItem
              v-for="project in projects"
              :key="project.id"
              :title="project.title"
              :description="project.description"
              :link="project.link"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>

</style>