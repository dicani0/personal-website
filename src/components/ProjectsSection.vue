<script setup>
import SectionHeading from "./SectionHeading.vue";
import ProjectItem from "./ProjectItem.vue";

const projects = [
  {
    title: "Game Manager",
    description: "Application for a game, that allows people to trade items, create characters and manage guilds",
    link: "https://github.com/dicani0/game-manager",
    technologies: [
      "PHP 8.3",
      "Laravel",
      "JavaScript",
      "TypeScript",
      "Vue.js",
      "Inertia",
      "Vite",
      "Tailwind CSS",
      "Pipelines Design Pattern",
      "MySQL",
      "Docker",
      "Websockets",
      "Laravel Echo",
      "Larastan",
      "GitHub Actions",
    ]
  },
  {
    title: "Laravel LMS (WIP)",
    description: "LMS application for managing courses",
    link: "https://github.com/dicani0/laravel-lms",
    technologies: [
      "PHP 8.3",
      "Laravel",
      "JavaScript",
      "TypeScript",
      "Vue.js",
      "Inertia",
      "Vite",
      "Tailwind CSS",
      "Domain Driven Design",
      "CQRS",
    ]
  },
  {
    title: "Task Manager (WIP)",
    description: "Task manager application with user authentication and authorization, that allows users to create, update, delete and list tasks.",
    link: "https://github.com/dicani0/task-manager-backend",
    technologies: [
      "Node.js",
      "Express",
      "TypeScript",
      "MongoDB",
      "Mongoose",
      "JWT",
    ]
  },
  {
    title: "Portfolio Website",
    description: "My personal website built with Vue.js and Tailwind CSS. Hosted on GitHub Pages.",
    link: "https://dicani0.github.io/personal-website/",
    technologies: [
      "Vue.js",
      "JavaScript",
      "Vite",
      "Tailwind CSS",
      "GitHub Pages",
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
              :technologies="project.technologies"
          />
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>

</style>