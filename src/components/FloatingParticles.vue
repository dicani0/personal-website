<script setup>
import {onMounted, ref} from "vue";

  const particles = ref([]);

  onMounted(() => {
    for (let i = 0; i < 100; i++) {
      const size = Math.ceil(Math.random() * 10) + 'px';
      const animationDuration = Math.ceil(Math.random() * 20) + 5 + 's';

      particles.value.push({
        id: i,
        style: {
          width: size,
          height: size,
          borderRadius: '50%',
          position: 'absolute',
          top: Math.random() * 100 + '%',
          left: Math.random() * 100 + '%',
          animationName: 'float',
          animationDuration: animationDuration,
          animationTimingFunction: 'linear',
          animationIterationCount: 'infinite',
          backgroundColor: 'rgba(76, 5, 25, 0.3)',
          boxShadow: '0 0 10px rgba(255, 0, 255, 0.1)',
        }
      });
    }
  });
</script>

<template>
  <div class="fixed inset-0 pointer-events-none">
    <div v-for="particle in particles" :key="particle.id" :style="particle.style" class="particle" style="z-index: -1"></div>
  </div>
</template>

<style>
.particle {
  animation: float 25s ease-in-out infinite;
  will-change: transform;
}

@keyframes float {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  25% {
    transform: translate(15vh, -15vh) scale(2.5)
  }
  50% {
    transform: translate(-10vh, 20vh) scale(0.8)
  }
  75% {
    transform: translate(-15vh, -10vh) scale(1.2)
  }
}

</style>