<script setup>
import {ref} from "vue";
import SectionHeading from "./SectionHeading.vue";
import axios from "axios";

const form = ref({
  name: "",
  email: "",
  message: ""
});

const message = ref("");
const result = ref("");

const submitForm = async () => {
  const data = {
    name: form.value.name,
    email: form.value.email,
    message: form.value.message
  };

  try {
    if (form.value.name === "" || form.value.email === "" || form.value.message === "") {
      message.value = "Please fill in all fields.";

      setTimeout(() => {
        message.value = "";
      }, 5000);

      return;
    }

    const res = await axios.post("https://formspree.io/f/mpzvkvbw", data);

    if (res.status === 200) {
      form.value.name = "";
      form.value.email = "";
      form.value.message = "";

      message.value = "Message sent successfully! I will get back to you soon.";
      result.value = "success";

      setTimeout(() => {
        message.value = "";
        result.value = "";
      }, 5000);

    } else {
      message.value = "An error occurred. Please try again later.";
      result.value = "error";

      setTimeout(() => {
        message.value = "";
        result.value = "";
      }, 5000);
    }
  } catch (e) {
    message.value = "An error occurred. Please try again later.";
    result.value = "error";

    setTimeout(() => {
      message.value = "";
      result.value = "";
    }, 5000);
  }
};
</script>

<template>
  <transition name="slide-fade">
    <p class="font-bold text-2xl fixed top-16 inset-x-0 p-4 ring-neutral-950 text-rose-300 text-center text-white transition ease-in-out delay-150 z-50"
       :class="{ 'bg-emerald-800': result === 'success', 'bg-rose-800': result === 'error'}"
       v-if="message !== ''">
      {{ message }}
    </p>
  </transition>
  <div class="container mx-auto px-4 min-h-dvh flex flex-col justify-center">
    <SectionHeading>
      Contact Me
    </SectionHeading>
    <section class="px-12 flex justify-center relative">
      <form @submit.prevent="submitForm" method="post"
            class="flex flex-col gap-4 w-full md:w-2/3 lg:w-3/5 shadow-lg rounded-lg shadow-rose-950 bg-neutral-950 relative p-6 z-20">
        <label for="name">Name</label>
        <input v-model="form.name" class="p-4" type="text" required name="name" placeholder="Your Name">
        <label for="email">Email</label>
        <input v-model="form.email" class="p-4" type="email" required name="email" placeholder="Your Email">
        <label for="message">Message</label>
        <textarea v-model="form.message" class="p-4" name="message" required placeholder="Your Message"></textarea>
        <button class="rounded p-4 bg-rose-950 hover:bg-rose-800 transition duration-300" type="submit">Send</button>
      </form>
    </section>
  </div>
</template>

<style scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: scale(0);
  opacity: 0;
}
</style>