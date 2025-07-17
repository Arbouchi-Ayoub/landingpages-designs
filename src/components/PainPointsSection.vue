<template>
  <div id="pain-points" class="bg-gray-50 dark:bg-gray-800 relative overflow-hidden">
    <!-- Decorative elements -->
    <div class="hidden lg:block absolute top-40 -right-20 w-96 h-96 bg-gradient-to-br from-red-50 to-red-100 dark:from-red-900 dark:to-red-800 rounded-full opacity-20 blur-3xl -z-10 animate-pulse-slow"></div>
    <div class="hidden lg:block absolute -bottom-20 -left-10 w-80 h-80 bg-gradient-to-tr from-orange-50 to-yellow-50 dark:from-orange-900 dark:to-yellow-900 rounded-full opacity-20 blur-3xl -z-10 animate-float"></div>
    <!-- Additional decorative blobs for visual interest -->
    <div class="hidden lg:block absolute top-60 left-20 w-48 h-48 bg-gradient-to-tl from-amber-50 to-amber-100 dark:from-amber-900 dark:to-amber-800 rounded-full opacity-15 blur-2xl -z-10" style="animation: float 9s ease-in-out infinite alternate; animation-delay: 1s;"></div>
    
    <div class="container mx-auto px-4 md:px-6 py-10 relative z-10">
      <!-- Section Header with enhanced animated reveal -->
      <div class="max-w-3xl mx-auto text-center mb-16 reveal">
        <div class="inline-block px-3 py-1 bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-400 text-sm font-medium rounded-full mb-4 transform transition hover:scale-105 hover:shadow-md">
          Problems Solved
        </div>
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 dark:text-white">
          Say Goodbye to <span class="text-gradient-red">Under-Sink Chaos</span>
        </h2>
        <p class="text-lg text-gray-600 dark:text-gray-400">
          We've addressed the most common kitchen organization frustrations with thoughtful design solutions
        </p>
      </div>
      
      <!-- Pain Points Cards with staggered animation -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-x-10 gap-y-16 mb-16 pain-points-grid">
        <!-- Pain Point 1 -->
        <div class="relative bg-white dark:bg-gray-900 rounded-2xl shadow-lg overflow-hidden border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl transform hover:-translate-y-1 hover:scale-[1.02] pain-point-card">
          <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-orange-500"></div>
          <div class="p-8">
            <div class="flex items-start">
              <div class="flex-shrink-0 mr-6">
                <div class="w-14 h-14 flex items-center justify-center rounded-full bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                  </svg>
                </div>
              </div>
              <div>
                <h3 class="text-xl font-bold mb-3 text-gray-900 dark:text-white">Can't Find Items in the Back</h3>
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-red-500 mr-3"></div>
                  <span class="text-sm text-red-600 dark:text-red-400 font-medium">THE PROBLEM</span>
                </div>
                <p class="text-gray-600 dark:text-gray-400 mb-6">
                  Items get lost in the back of cabinets, forcing you to bend down, use flashlights, or empty everything just to find what you need
                </p>
                
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-green-500 mr-3"></div>
                  <span class="text-sm text-green-600 dark:text-green-400 font-medium">OUR SOLUTION</span>
                </div>
                <p class="text-gray-700 dark:text-gray-300">
                  Smooth-gliding drawers extend fully, bringing everything into clear view and easy reach — no more digging or lost items
                </p>
              </div>
            </div>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 px-8 py-4 border-t border-gray-200 dark:border-gray-700">
            <div class="flex items-center">
              <svg class="h-5 w-5 text-green-500 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <span class="text-sm font-medium text-gray-600 dark:text-gray-400">100% visibility of all stored items</span>
            </div>
          </div>
        </div>
        
        <!-- Pain Point 2 -->
        <div class="relative bg-white dark:bg-gray-900 rounded-2xl shadow-lg overflow-hidden border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl transform hover:-translate-y-1 hover:scale-[1.02] pain-point-card">
          <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-orange-500"></div>
          <div class="p-8">
            <div class="flex items-start">
              <div class="flex-shrink-0 mr-6">
                <div class="w-14 h-14 flex items-center justify-center rounded-full bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
                  </svg>
                </div>
              </div>
              <div>
                <h3 class="text-xl font-bold mb-3 text-gray-900 dark:text-white">Water Damage & Mold</h3>
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-red-500 mr-3"></div>
                  <span class="text-sm text-red-600 dark:text-red-400 font-medium">THE PROBLEM</span>
                </div>
                <p class="text-gray-600 dark:text-gray-400 mb-6">
                  Under-sink areas are prone to moisture from leaks or humidity, damaging organizers and creating health hazards from mold and mildew
                </p>
                
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-green-500 mr-3"></div>
                  <span class="text-sm text-green-600 dark:text-green-400 font-medium">OUR SOLUTION</span>
                </div>
                <p class="text-gray-700 dark:text-gray-300">
                  Our specialized water-resistant materials include antimicrobial properties that prevent mold growth even in humid conditions
                </p>
              </div>
            </div>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 px-8 py-4 border-t border-gray-200 dark:border-gray-700">
            <div class="flex items-center">
              <svg class="h-5 w-5 text-green-500 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <span class="text-sm font-medium text-gray-600 dark:text-gray-400">Mold-resistant surface treatment</span>
            </div>
          </div>
        </div>
        
        <!-- Pain Point 3 -->
        <div class="relative bg-white dark:bg-gray-900 rounded-2xl shadow-lg overflow-hidden border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl transform hover:-translate-y-1 hover:scale-[1.02] pain-point-card">
          <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-orange-500"></div>
          <div class="p-8">
            <div class="flex items-start">
              <div class="flex-shrink-0 mr-6">
                <div class="w-14 h-14 flex items-center justify-center rounded-full bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
                  </svg>
                </div>
              </div>
              <div>
                <h3 class="text-xl font-bold mb-3 text-gray-900 dark:text-white">Awkward Cabinet Fit</h3>
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-red-500 mr-3"></div>
                  <span class="text-sm text-red-600 dark:text-red-400 font-medium">THE PROBLEM</span>
                </div>
                <p class="text-gray-600 dark:text-gray-400 mb-6">
                  Standard organizers rarely fit around pipes and plumbing fixtures, wasting precious space and leaving odd gaps
                </p>
                
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-green-500 mr-3"></div>
                  <span class="text-sm text-green-600 dark:text-green-400 font-medium">OUR SOLUTION</span>
                </div>
                <p class="text-gray-700 dark:text-gray-300">
                  Our patented expandable width (15"-25") and adjustable shelving adapts to work around pipes and unusual cabinet shapes
                </p>
              </div>
            </div>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 px-8 py-4 border-t border-gray-200 dark:border-gray-700">
            <div class="flex items-center">
              <svg class="h-5 w-5 text-green-500 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <span class="text-sm font-medium text-gray-600 dark:text-gray-400">Fits 97% of standard cabinets</span>
            </div>
          </div>
        </div>
        
        <!-- Pain Point 4 -->
        <div class="relative bg-white dark:bg-gray-900 rounded-2xl shadow-lg overflow-hidden border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl transform hover:-translate-y-1 hover:scale-[1.02] pain-point-card">
          <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-orange-500"></div>
          <div class="p-8">
            <div class="flex items-start">
              <div class="flex-shrink-0 mr-6">
                <div class="w-14 h-14 flex items-center justify-center rounded-full bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
              </div>
              <div>
                <h3 class="text-xl font-bold mb-3 text-gray-900 dark:text-white">Difficult Installation</h3>
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-red-500 mr-3"></div>
                  <span class="text-sm text-red-600 dark:text-red-400 font-medium">THE PROBLEM</span>
                </div>
                <p class="text-gray-600 dark:text-gray-400 mb-6">
                  Many organizers require complicated assembly, special tools, or even drilling into cabinet walls, causing frustration and damage
                </p>
                
                <div class="mb-4 flex items-center">
                  <div class="h-0.5 w-12 bg-green-500 mr-3"></div>
                  <span class="text-sm text-green-600 dark:text-green-400 font-medium">OUR SOLUTION</span>
                </div>
                <p class="text-gray-700 dark:text-gray-300">
                  Tool-free installation with intuitive click-together assembly allows for setup in under 5 minutes with zero cabinet modifications
                </p>
              </div>
            </div>
          </div>
          <div class="bg-gray-50 dark:bg-gray-800 px-8 py-4 border-t border-gray-200 dark:border-gray-700">
            <div class="flex items-center">
              <svg class="h-5 w-5 text-green-500 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <span class="text-sm font-medium text-gray-600 dark:text-gray-400">No tools or hardware required</span>
            </div>
          </div>
        </div>
      </div>
      
      <!-- CTA Block with animation -->
      <div class="text-center mt-12 cta-container">
        <a href="#" class="inline-block px-8 py-4 bg-gradient-to-r from-primary-600 to-primary-500 hover:from-primary-700 hover:to-primary-600 text-white font-bold rounded-lg shadow-lg hover:shadow-xl transform transition duration-500 hover:-translate-y-1 hover:scale-105 animate-pulse-subtle cta-button group">
          <span class="relative z-10 flex items-center justify-center group-hover:scale-105 transition-transform duration-300">
            Solve Your Storage Problems Today
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2 transform transition-transform duration-300 group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  name: 'PainPointsSection',
  setup() {
    const isVisible = ref(false);
    
    onMounted(() => {
      const painPointsSection = document.getElementById('pain-points');
      if (painPointsSection) {
        const stop = useIntersectionObserver(
          painPointsSection,
          ([{ isIntersecting }]) => {
            if (isIntersecting) {
              isVisible.value = true;
              
              // Animate section header
              const header = document.querySelector('.section-header');
              if (header) header.classList.add('visible');
              
              // Animate pain point cards with staggered delay
              const cards = document.querySelectorAll('.pain-point-card');
              cards.forEach((card, index) => {
                setTimeout(() => {
                  card.classList.add('visible');
                }, 300 + (index * 150));
              });
              
              // Animate CTA with delay
              setTimeout(() => {
                const cta = document.querySelector('.cta-container');
                if (cta) cta.classList.add('visible');
              }, 300 + (cards.length * 150));
              
              // Stop observing once triggered
              stop();
            }
          },
          { threshold: 0.15 }
        );
      }
    });
    
    return {
      isVisible
    };
  },
  data() {
    return {
      painPoints: [
        {
          icon: '🔍',
          concern: 'Hard to find items in the back?',
          solution: 'Our sliding drawers pull out completely so you can easily see and reach everything stored in the back of your cabinet.'
        },
        {
          icon: '💧',
          concern: 'Worried about water damage?',
          solution: 'Our organizer is made with water-resistant materials specially designed for under-sink environments where occasional spills happen.'
        },
        {
          icon: '📐',
          concern: 'Not sure if it will fit your cabinet?',
          solution: 'With our adjustable design, you can customize the width and height to fit most standard under-sink cabinets, even with plumbing obstacles.'
        },
        {
          icon: '🔨',
          concern: 'Concerned about difficult installation?',
          solution: 'No special tools needed! Our organizer comes with simple instructions and all necessary hardware for a quick 15-minute installation.'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* Section header animations - improved timing and easing */
.section-header {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.9s cubic-bezier(0.16, 1, 0.3, 1); /* Use a more modern easing */
}

.section-header.visible {
  opacity: 1;
  transform: translateY(0);
}

.badge-animated, .title-animated, .description-animated {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.7s cubic-bezier(0.34, 1.56, 0.64, 1); /* Bouncy, more dynamic easing */
  will-change: transform, opacity; /* Performance optimization */
}

.section-header.visible .badge-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.15s;
}

.section-header.visible .title-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.3s;
}

.section-header.visible .description-animated {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.45s;
}

/* Pain point cards animations */
.pain-point-card {
  opacity: 0;
  transform: translateY(40px) scale(0.95);
  transition: all 0.6s cubic-bezier(0.5, 0, 0.1, 1);
}

.pain-point-card.visible {
  opacity: 1;
  transform: translateY(0) scale(1);
}

.problem-line {
  position: relative;
  overflow: hidden;
}

.problem-line::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
  animation: shimmer 3s infinite;
}

@keyframes shimmer {
  0% { left: -100%; }
  100% { left: 100%; }
}

.icon-container {
  position: relative;
  transition: all 0.4s cubic-bezier(0.5, 0, 0.1, 1);
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.pain-point-card:hover .icon-container {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* CTA animations */
.cta-container {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

.cta-container.visible {
  opacity: 1;
  transform: translateY(0);
}

.cta-button {
  position: relative;
  overflow: hidden;
}

.cta-button:before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.3) 0%, transparent 70%);
  opacity: 0;
  transform: scale(0.5);
  transition: opacity 0.5s, transform 0.5s;
}

.cta-button:hover:before {
  opacity: 1;
  transform: scale(1);
}

/* Text gradient effect */
/* Text gradient effect */
.text-gradient-red {
  background: linear-gradient(90deg, #EF4444, #F59E0B);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
}

/* Floating animation for decorative elements */
.animate-float {
  animation: float 8s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 6s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.animate-pulse-subtle {
  animation: pulse-subtle 3s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
  100% { transform: translateY(0px); }
}

@keyframes pulse-slow {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.15; transform: scale(1.1); }
}

@keyframes pulse-subtle {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.02); }
}
</style>
