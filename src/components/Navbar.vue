<script setup>
import NavbarItem from "./NavbarItem.vue";
import {ref} from "vue";

const isOpen = ref(false);

const sections = [
  {type: "home", title: "Home", section: "#home"},
  {type: "info", title: "About me", section: "#about"},
  {type: "cpu", title: "Skills", section: "#skills"},
  {type: "briefcase", title: "Experience", section: "#experience"},
  {type: "trending-up", title: "Projects", section: "#projects"},
  {type: "mail", title: "Contact", section: "#contact"}
];

</script>

<template>
  <nav class="sticky top-0 bg-rose-950 opacity-95 z-10">
    <div class="container mx-auto px-4 py-4">
      <div class="flex items-center">
        <button @click="isOpen = !isOpen" class="text-white focus:outline-none mr-4 lg:hidden">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6h16.5m-16.5 6h16.5m-16.5 6h16.5"/>
          </svg>
        </button>
      </div>
      <transition name="menu">
        <ul class="transition-opacity duration-500 ease-in-out flex-col flex lg:flex lg:flex-row gap-4 justify-between items-center transition ease-in-out delay-150 duration-1000"
            :class="{'hidden': !isOpen, 'block':isOpen}"
        >
          <NavbarItem v-for="section in sections" :key="section.type" :type="section.type" :title="section.title"
                      :section="section.section"/>
        </ul>
      </transition>
    </div>
  </nav>
</template>

<style scoped>
.menu-enter-active, .menu-leave-active {
  transition: opacity 1.5s;
}
.menu-enter-from, .menu-leave-to {
  opacity: 0;
}
.menu-enter-to, .menu-leave-from {
  opacity: 1;
}
</style>