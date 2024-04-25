<script setup>
import NavbarItem from "./NavbarItem.vue";

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
  <nav class="sticky top-0 bg-rose-950 opacity-80" style="z-index: 1000">
    <div class="container mx-auto px-4 py-4">
      <ul class="flex flex-row gap-4 justify-between">
        <NavbarItem v-for="section in sections" :key="section.type" :type="section.type" :title="section.title"
                    :section="section.section"/>
      </ul>
    </div>
  </nav>
</template>
