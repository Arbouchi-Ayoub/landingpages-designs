<template>
  <div class="min-h-screen bg-gray-50 dark:bg-gray-900">
    <LandingPage />
  </div>
</template>

<style>
/* Global Animation Classes */
.fade-up-enter-active,
.fade-up-leave-active {
  transition: opacity 0.8s ease, transform 0.8s ease;
}

.fade-up-enter-from,
.fade-up-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

/* Animation for elements on scroll */
.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Staggered child animations */
.stagger-reveal > * {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.5s ease, transform 0.5s ease;
}

.stagger-reveal.visible > *:nth-child(1) { transition-delay: 0.1s; }
.stagger-reveal.visible > *:nth-child(2) { transition-delay: 0.2s; }
.stagger-reveal.visible > *:nth-child(3) { transition-delay: 0.3s; }
.stagger-reveal.visible > *:nth-child(4) { transition-delay: 0.4s; }
.stagger-reveal.visible > *:nth-child(5) { transition-delay: 0.5s; }
.stagger-reveal.visible > *:nth-child(6) { transition-delay: 0.6s; }

.stagger-reveal.visible > * {
  opacity: 1;
  transform: translateY(0);
}

/* Fade in animation */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

/* Slide in animation */
@keyframes slide-in-from-left {
  from { transform: translateX(-100%); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

@keyframes slide-in-from-right {
  from { transform: translateX(100%); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

@keyframes slideInRight {
  from { transform: translateX(50px); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

@keyframes slideInLeft {
  from { transform: translateX(-50px); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

@keyframes shimmer-once {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

@keyframes pulse-slow {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0px); }
}

@keyframes spin-slow {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.animate-shimmer-once {
  animation: shimmer-once 1s forwards;
}

.animate-pulse-slow {
  animation: pulse-slow 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-spin-slow {
  animation: spin-slow 8s linear infinite;
}

/* Pulse animation */
@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.05); }
  100% { transform: scale(1); }
}
</style>

<script>
import LandingPage from './views/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  },
  mounted() {
    // Initialize dark mode based on localStorage preference or system preference
    if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  }
}
</script>
