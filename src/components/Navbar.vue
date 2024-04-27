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

const toggleNavbar = () => {
  isOpen.value = !isOpen.value;
};

</script>

<template>
  <div class="bg-transparent fixed w-full top-0 z-50">

    <!--Normal Navbar-->
    <nav class="hidden lg:flex sticky top-0 bg-rose-950 opacity-95 z-10">
      <div class="container mx-auto px-4 py-4">
        <ul class="flex-col hidden lg:flex lg:flex-row gap-4 justify-between items-center transition ease-in-out delay-150">
          <NavbarItem v-for="section in sections" :key="section.type" :type="section.type" :title="section.title"
                      :section="section.section"/>
        </ul>
      </div>
    </nav>

    <!--Mobile Navbar-->
    <div class="bg-rose-950">
      <button @click="toggleNavbar" class="text-white focus:outline-none w-full lg:hidden">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
             stroke="currentColor" class="w-full h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6h16.5m-16.5 6h16.5m-16.5 6h16.5"/>
        </svg>
      </button>
    </div>

    <transition name="slide" mode="out-in">
      <nav v-if="isOpen" class="transition ease-in-out delay-150 block lg:hidden sticky bg-rose-950 top-0 opacity-95 z-10">
        <div class="transition ease-in-out delay-150  container mx-auto bg-rose-950 px-4 py-4">
          <div class="flex items-center">
          </div>
          <div v-if="isOpen" class="transition ease-in-out delay-150">
            <ul class="flex-col flex lg:hidden gap-4 justify-between items-center">
              <NavbarItem v-for="section in sections" :key="section.type" :type="section.type" :title="section.title"
                          :section="section.section"/>
            </ul>
          </div>
        </div>
      </nav>
    </transition>
  </div>
</template>

<style scoped>
.container {
  transition: all 0.3s ease-in-out;
}

.slide-enter-active, .slide-leave-active {
  transition: transform 0.3s ease-in-out;
}

.slide-enter-from, .slide-leave-to {
  transform: translateY(-100%);
}
</style>