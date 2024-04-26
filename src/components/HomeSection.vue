<script setup>
</script>

<template>
  <div class="container mx-auto px-4 min-h-dvh flex flex-col justify-center">
    <section class="text-center space-y-4 py-10">
      <div class="w-60 h-60 bg-neutral-900 opacity-80 mx-auto flex rounded-full items-center bg-neutral-900 border-2 border-rose-900 ring">
        <img src="@/assets/profile.webp" alt="Your Name" class="mx-auto w-48 h-48 object-cover rounded-full">
      </div>
      <h1 class="text-4xl font-bold text-gray-200 relative bg-neutral-350">Hello, I'm Dawid!</h1>
      <p class="text-xl text-gray-300 relative bg-neutral-950">Professional Web Developer Specializing in Laravel</p>
    </section>

    <section class="text-center py-6">
      <p class="text-gray-400 relative bg-neutral-950">Welcome to my personal website. Here you can find details about my projects, skills, and
        professional experience. Take a look around and get in touch!</p>
    </section>

    <section class="flex gap-8 justify-center space-x-4 py-6 text-white">
      <a href="https://github.com/dicani0" target="_blank" class="transition text-white hover:text-rose-900 flex gap-1 relative bg-neutral-950">
        <vue-feather type="github"></vue-feather>
        <span>GitHub</span>
      </a>
      <a href="https://www.linkedin.com/in/dawid-miklas/" target="_blank"
         class="transition text-white hover:text-rose-900 flex gap-1 relative bg-neutral-950">
        <vue-feather type="linkedin"></vue-feather>
        <span>LinkedIn</span>
      </a>
    </section>
  </div>
</template>

<style scoped>
@keyframes pulse {
  0% {
    box-shadow: 0 0 0 0 rgb(136, 19, 55);
  }
  100% {
    box-shadow: 0 0 0 10px rgba(136, 19, 55, 0);
  }
}

.container .ring {
  animation: pulse 1s infinite;
  box-shadow: 0 0 0 0 rgba(255, 0, 0, 0);
  transition: box-shadow 0.3s ease-in-out;
}
</style>