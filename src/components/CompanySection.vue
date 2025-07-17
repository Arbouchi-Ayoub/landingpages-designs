<template>
  <div id="company" class="relative overflow-hidden">
    <!-- Enhanced decorative elements for visual interest -->
    <div class="hidden lg:block absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-blue-50 to-primary-50 dark:from-blue-900 dark:to-primary-900 rounded-full opacity-30 blur-3xl -z-10 animate-float-slow"></div>
    <div class="hidden lg:block absolute bottom-20 left-10 w-80 h-80 bg-gradient-to-tr from-purple-50 to-indigo-50 dark:from-purple-900 dark:to-indigo-900 rounded-full opacity-20 blur-3xl -z-10 animate-float-reverse"></div>
    <div class="hidden lg:block absolute top-1/2 left-1/4 w-24 h-24 bg-gradient-to-br from-cyan-50 to-teal-50 dark:from-cyan-900 dark:to-teal-900 rounded-full opacity-20 blur-xl -z-10" style="animation: float 7s ease-in-out infinite alternate; animation-delay: 2s;"></div>
      
    <!-- Section Header with animation --> 
    <div class="max-w-3xl mx-auto text-center mb-16 reveal">
      <div class="inline-block px-3 py-1 bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 text-sm font-medium rounded-full mb-4 transform transition hover:scale-105 hover:shadow-md">
        Our Story
      </div>
      <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 dark:text-white">
        About <span class="text-gradient">OrganizeMax</span>
      </h2>
      <p class="text-lg text-gray-600 dark:text-gray-400">
        The brand home organization experts trust.
      </p>
    </div>
    
    <!-- Main Content Area -->
    <div class="flex flex-col md:flex-row gap-8 items-center max-w-6xl mx-auto">
      <div class="md:w-1/3 image-container">
        <div class="relative overflow-hidden rounded-lg shadow-lg">
          <img 
            src="https://images.unsplash.com/photo-1556157382-97eda2d62296?auto=format&fit=crop&q=80&w=1470" 
            alt="OrganizeMax Team" 
            class="w-full h-auto transform transition-transform duration-700 hover:scale-105"
          />
          <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500 flex items-end">
            <div class="p-4 text-white z-20">
              <p class="font-medium text-white">The OrganizeMax Team</p>
              <p class="text-sm text-white opacity-80">Passionate about organization & design</p>
            </div>
          </div>
        </div>
      </div>
      
      <div class="md:w-2/3 content-text">
        <p class="text-gray-600 dark:text-gray-300 mb-4 animated-text">
          Founded in 2020, OrganizeMax was born from a simple idea: everyone deserves a well-organized home without breaking the bank. Our team of design and organization experts has over 25 years of combined experience creating practical storage solutions.
        </p>
        <p class="text-gray-600 dark:text-gray-300 mb-6 animated-text" style="transition-delay: 0.2s;">
          We believe in quality, sustainability, and thoughtful design that makes everyday life easier. Our products are tested rigorously to ensure they stand up to daily use while maintaining their functionality and appearance.
        </p>
        
        <div class="flex flex-wrap gap-6 stats-container">
          <div v-for="(stat, index) in companyStats" :key="index" 
               class="text-center p-4 bg-white dark:bg-gray-800 rounded-lg shadow-md transform transition-all duration-300 hover:-translate-y-1 hover:shadow-lg stat-card"
               :style="{ transitionDelay: `${index * 100}ms` }">
            <div class="text-3xl font-bold text-primary-600 dark:text-primary-400 counter-value">{{ stat.value }}</div>
            <div class="text-sm text-gray-600 dark:text-gray-400">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Values section with animation -->
    <div class="mt-16 mb-8 values-container max-w-6xl mx-auto">
      <h3 class="text-2xl font-bold text-center mb-8 values-header">Our Core Values</h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div v-for="(value, index) in coreValues" :key="index" 
             class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md transform transition-all duration-500 hover:-translate-y-2 hover:shadow-lg value-card"
             :style="{ transitionDelay: `${index * 150}ms` }">
          <div class="w-12 h-12 flex items-center justify-center rounded-full bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 mb-4">
            <i :class="value.icon" class="text-xl"></i>
          </div>
          <h4 class="text-xl font-bold mb-2 text-gray-900 dark:text-white">{{ value.title }}</h4>
          <p class="text-gray-600 dark:text-gray-300">{{ value.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  name: 'CompanySection',
  data() {
    return {
      companyStats: [
        { value: '100K+', label: 'Happy Customers' },
        { value: '4.8/5', label: 'Average Rating' },
        { value: '15+', label: 'Product Awards' },
        { value: '50+', label: 'Countries Shipped To' }
      ],
      coreValues: [
        { 
          icon: 'fas fa-gem', 
          title: 'Quality', 
          description: 'We use premium materials and rigorous testing to ensure our products last for years.' 
        },
        { 
          icon: 'fas fa-leaf', 
          title: 'Sustainability', 
          description: 'Our products are made with eco-friendly materials and minimal packaging waste.' 
        },
        { 
          icon: 'fas fa-lightbulb', 
          title: 'Innovation', 
          description: 'We continuously improve our designs based on customer feedback and new technologies.' 
        }
      ],
      sectionVisible: false,
      animationComplete: false
    };
  },
  methods: {
    setupAnimations() {
      // Set up intersection observer for the reveal animations using VueUse
      const companySection = document.querySelector('#company');
      
      if (companySection) {
        const stop = useIntersectionObserver(
          companySection,
          ([{ isIntersecting }]) => {
            if (isIntersecting) {
              this.sectionVisible = true;
              // Start animations when section comes into view
              this.animateElements();
              // Stop observing after triggering
              stop();
            }
          },
          { threshold: 0.2 }
        );
      } else {
        // Fallback if element not found
        this.sectionVisible = true;
        this.animateElements();
      }
    },
    animateElements() {
      // Add animation to all elements with reveal class
      const revealElements = document.querySelectorAll('.reveal');
      revealElements.forEach((el, i) => {
        setTimeout(() => {
          el.classList.add('section-visible');
        }, i * 150);
      });
      
      // Animate image container and content text
      setTimeout(() => {
        const imgContainer = document.querySelector('.image-container');
        const content = document.querySelector('.content-text');
        
        if (imgContainer) imgContainer.classList.add('visible');
        if (content) content.classList.add('visible');
        
        // Animate stats cards with staggered delay
        const statCards = document.querySelectorAll('.stat-card');
        statCards.forEach((card, index) => {
          setTimeout(() => {
            card.classList.add('visible');
          }, 200 + (index * 100)); // Faster animation timing
        });
        
        // Animate values section
        setTimeout(() => {
          const valuesHeader = document.querySelector('.values-header');
          if (valuesHeader) valuesHeader.classList.add('visible');
          
          // Animate value cards with staggered delay
          const valueCards = document.querySelectorAll('.value-card');
          valueCards.forEach((card, index) => {
            setTimeout(() => {
              card.classList.add('visible');
            }, 100 + (index * 100)); // Faster animation timing
          });
        }, 400); // Reduced delay
      }, 200); // Reduced delay
      
      setTimeout(() => {
        this.animationComplete = true;
      }, 1200); // Faster completion time
    }
  },
  mounted() {
    this.setupAnimations();
  }
}
</script>

<style scoped>
/* Section header animations */
.section-header {
  opacity: 0;
  transform: translateY(30px);
  transition: all 1s cubic-bezier(0.5, 0, 0.1, 1);
}

.section-header.visible {
  opacity: 1;
  transform: translateY(0);
}

.badge-animated, .title-animated, .description-animated {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

.section-header.visible .badge-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.2s;
}

.section-header.visible .title-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.4s;
}

.section-header.visible .description-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.6s;
}

/* Text gradient effect */
.text-gradient {
  background: linear-gradient(90deg, #3B82F6, #8B5CF6);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
}

/* Content animations - improved with better easing */
.image-container, .content-text {
  opacity: 0;
  transition: all 0.9s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: transform, opacity; /* Performance optimization */
}

.image-container {
  transform: translateX(-40px);
}

.content-text {
  transform: translateX(40px);
}

.image-container.visible, .content-text.visible {
  opacity: 1;
  transform: translateX(0);
}

.animated-text {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.content-text.visible .animated-text {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.15s;
}

/* Stats card animations */
.stat-card {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.6s cubic-bezier(0.5, 0, 0.1, 1);
}

.stat-card.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Values section animations */
.values-header {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

.values-header.visible {
  opacity: 1;
  transform: translateY(0);
}

.value-card {
  opacity: 0;
  transform: translateY(40px) scale(0.95);
  transition: all 0.7s cubic-bezier(0.5, 0, 0.1, 1);
}

.value-card.visible {
  opacity: 1;
  transform: translateY(0) scale(1);
}

/* Decorative animations */
.animate-float-slow {
  animation: float 10s ease-in-out infinite;
}

.animate-float-reverse {
  animation: float-reverse 8s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(20px); }
  100% { transform: translateY(0px); }
}

@keyframes float-reverse {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}

/* Counter animation effect */
.counter-value {
  transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.stat-card:hover .counter-value {
  transform: scale(1.2);
  color: #4F46E5; /* Indigo-600 highlight on hover */
}

/* Support for section-visible class used by LandingPage.vue */
.section-visible {
  opacity: 1;
  transform: translateY(0);
}

.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}
</style>
