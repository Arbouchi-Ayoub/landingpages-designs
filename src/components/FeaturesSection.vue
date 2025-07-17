<template>
  <div id="features" class="bg-white dark:bg-gray-900 relative overflow-hidden">
    <!-- Enhanced decorative elements -->
    <div class="hidden lg:block absolute top-40 right-0 w-72 h-72 bg-gradient-to-br from-primary-50 to-primary-100 dark:from-primary-900 dark:to-primary-800 rounded-full opacity-20 blur-3xl -z-10 animate-pulse-slow"></div>
    <div class="hidden lg:block absolute bottom-20 left-10 w-96 h-96 bg-gradient-to-tr from-blue-50 to-green-50 dark:from-blue-900 dark:to-green-900 rounded-full opacity-20 blur-3xl -z-10 animate-float"></div>
    <div class="hidden lg:block absolute top-1/3 left-1/4 w-32 h-32 bg-gradient-to-tl from-indigo-50 to-purple-50 dark:from-indigo-900 dark:to-purple-900 rounded-full opacity-15 blur-2xl -z-10" style="animation: float 8s ease-in-out infinite alternate; animation-delay: 1.5s;"></div>
    <div class="hidden lg:block absolute bottom-1/3 right-1/4 w-24 h-24 bg-gradient-to-br from-cyan-50 to-sky-50 dark:from-cyan-900 dark:to-sky-900 rounded-full opacity-20 blur-xl -z-10" style="animation: float 7s ease-in-out infinite alternate-reverse; animation-delay: 0.8s;"></div>
    
    <div class="relative z-10">
      <!-- Section Header with animated reveal -->
      <div class="max-w-3xl mx-auto text-center mb-16 section-header">
        <div class="inline-block px-3 py-1 bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 text-sm font-medium rounded-full mb-4 badge-animated">
          Smart Design
        </div>
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 dark:text-white title-animated">
          Why Our <span class="text-gradient">Under-Sink Organizer</span> Stands Out
        </h2>
        <p class="text-lg text-gray-600 dark:text-gray-400 description-animated">
          Engineered to transform cluttered spaces into functional storage with premium features that make organization effortless
        </p>
      </div>
      
      <!-- Features Grid with staggered animation -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 features-grid">
        <!-- Feature 1: Expandable Design -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-primary-300 dark:hover:border-primary-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-primary-500 to-primary-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 8V4m0 0h4M4 4l5 5m11-1V4m0 0h-4m4 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5v-4m0 4h-4m4 0l-5-5" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-primary-600 dark:group-hover:text-primary-400 transition-colors">
                Expandable Design
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Adjusts from 15" to 25" width to fit almost any cabinet size perfectly, maximizing your available space
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-primary-600 dark:text-primary-400">Perfect fit guarantee</span>
              <div class="h-1.5 w-1.5 rounded-full bg-primary-500"></div>
            </div>
          </div>
        </div>

        <!-- Feature 2: Smooth Sliding Drawers -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-primary-300 dark:hover:border-primary-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-primary-500 to-primary-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M7 11l5-5m0 0l5 5m-5-5v12" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-primary-600 dark:group-hover:text-primary-400 transition-colors">
                Smooth Sliding Drawers
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Premium ball-bearing slides ensure drawers glide effortlessly, giving you instant access to all your items
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-primary-600 dark:text-primary-400">Lifetime slide warranty</span>
              <div class="h-1.5 w-1.5 rounded-full bg-primary-500"></div>
            </div>
          </div>
        </div>

        <!-- Feature 3: Durable Construction -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-primary-300 dark:hover:border-primary-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-primary-500 to-primary-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-primary-600 dark:group-hover:text-primary-400 transition-colors">
                Durable Construction
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Built with heavy-duty powder-coated steel and BPA-free plastic for years of reliable daily use
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-primary-600 dark:text-primary-400">5-year quality guarantee</span>
              <div class="h-1.5 w-1.5 rounded-full bg-primary-500"></div>
            </div>
          </div>
        </div>

        <!-- Feature 4: Easy Installation -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-primary-300 dark:hover:border-primary-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-green-500 to-green-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-green-600 dark:group-hover:text-green-400 transition-colors">
                Tool-Free Installation
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Sets up in under 5 minutes with simple click-together assembly — no tools or hardware required
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-green-600 dark:text-green-400">Easiest setup in category</span>
              <div class="h-1.5 w-1.5 rounded-full bg-green-500"></div>
            </div>
          </div>
        </div>

        <!-- Feature 5: Modular Design -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-primary-300 dark:hover:border-primary-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-primary-500 to-primary-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-primary-600 dark:group-hover:text-primary-400 transition-colors">
                Customizable System
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Stack multiple units or add optional drawer dividers to create a personalized organization solution
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-primary-600 dark:text-primary-400">Compatible with all accessories</span>
              <div class="h-1.5 w-1.5 rounded-full bg-primary-500"></div>
            </div>
          </div>
        </div>

        <!-- Feature 6: Water-Resistant -->
        <div class="relative group feature-card">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-2xl border border-gray-200 dark:border-gray-700 transition-all duration-500 hover:shadow-xl hover:border-blue-300 dark:hover:border-blue-700 h-full transform hover:-translate-y-2 hover:scale-[1.01] feature-card-inner">
            <div class="absolute -top-5 left-5 bg-gradient-to-br from-blue-500 to-blue-700 p-4 rounded-2xl shadow-lg text-white feature-icon transform transition-all duration-500 group-hover:scale-110 group-hover:rotate-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4" />
              </svg>
            </div>
            <div class="mt-6 mb-4">
              <h3 class="text-xl font-bold mb-2 text-gray-900 dark:text-white group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors">
                Water-Resistant Materials
              </h3>
              <p class="text-gray-600 dark:text-gray-400">
                Specially designed for under-sink environments with materials that resist moisture, mold and mildew
              </p>
            </div>
            <div class="mt-6 flex items-center justify-between">
              <span class="text-sm font-semibold text-blue-600 dark:text-blue-400">Anti-microbial protection</span>
              <div class="h-1.5 w-1.5 rounded-full bg-blue-500"></div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Feature Highlight -->
      <div class="mt-20 bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-800 dark:to-gray-900 rounded-2xl overflow-hidden shadow-xl highlight-feature transform transition-all duration-500 hover:shadow-2xl hover:scale-[1.01] hover:-translate-y-1">
        <div class="flex flex-col md:flex-row highlight-container">
          <div class="md:w-1/2 p-8 md:p-12 highlight-content">
            <div class="inline-block px-3 py-1 bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 text-sm font-medium rounded-full mb-4 highlight-badge">
              Featured Highlight
            </div>
            <h3 class="text-2xl md:text-3xl font-bold mb-6 text-gray-900 dark:text-white highlight-title">
              <span class="text-gradient">Revolutionary</span> Adjustable Height Technology
            </h3>
            <p class="text-lg text-gray-600 dark:text-gray-400 mb-8 highlight-description">
              Our patent-pending height adjustment system allows you to customize each shelf independently, creating the perfect fit for tall bottles, small containers, and everything in between.
            </p>
            <ul class="space-y-4 highlight-list">
              <li class="flex items-center highlight-item">
                <span class="mr-4 flex-shrink-0 text-green-500 highlight-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                  </svg>
                </span>
                <span class="text-gray-700 dark:text-gray-300">5-level adjustment for each shelf</span>
              </li>
              <li class="flex items-center highlight-item">
                <span class="mr-4 flex-shrink-0 text-green-500 highlight-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                  </svg>
                </span>
                <span class="text-gray-700 dark:text-gray-300">Tool-free height changes in seconds</span>
              </li>
              <li class="flex items-center highlight-item">
                <span class="mr-4 flex-shrink-0 text-green-500 highlight-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                  </svg>
                </span>
                <span class="text-gray-700 dark:text-gray-300">Accommodates items up to 15" tall</span>
              </li>
            </ul>
          </div>
          <div class="md:w-1/2 bg-gray-200 dark:bg-gray-700 highlight-image-container overflow-hidden">
            <img 
              src="/src/assets/product-images/expandable-width.jpg" 
              alt="Expandable Width Demonstration" 
              class="w-full h-full object-cover transition-transform duration-700 hover:scale-105 highlight-image"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  name: 'FeaturesSection',
  setup() {
    const isVisible = ref(false);
    
    onMounted(() => {
      const featuresSection = document.getElementById('features');
      if (featuresSection) {
        const stop = useIntersectionObserver(
          featuresSection,
          ([{ isIntersecting }]) => {
            if (isIntersecting) {
              isVisible.value = true;
              
              // Animate section header
              const header = document.querySelector('.section-header');
              if (header) header.classList.add('visible');
              
              // Animate feature cards with staggered delay
              const cards = document.querySelectorAll('.feature-card');
              cards.forEach((card, index) => {
                setTimeout(() => {
                  card.classList.add('visible');
                }, 100 + (index * 150));
              });
              
              // Setup highlight feature animations
              const highlightFeature = document.querySelector('.highlight-feature');
              if (highlightFeature) {
                const stopHighlight = useIntersectionObserver(
                  highlightFeature,
                  ([{ isIntersecting }]) => {
                    if (isIntersecting) {
                      // Animate highlight content elements with staggered delay
                      const elements = [
                        '.highlight-badge',
                        '.highlight-title',
                        '.highlight-description',
                        '.highlight-item'
                      ];
                      
                      elements.forEach((selector, index) => {
                        const elems = document.querySelectorAll(selector);
                        elems.forEach((el, i) => {
                          setTimeout(() => {
                            el.classList.add('visible');
                          }, 200 + ((index * 3 + i) * 100));
                        });
                      });
                      
                      // Animate image
                      const image = document.querySelector('.highlight-image');
                      if (image) image.classList.add('visible');
                      
                      stopHighlight();
                    }
                  },
                  { threshold: 0.15 }
                );
              }
              
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
      features: [
        {
          icon: '📦',
          title: 'Maximizes Space',
          description: 'Our sliding drawer design utilizes every inch of your under-sink area, doubling your storage capacity.'
        },
        {
          icon: '🔧',
          title: 'Easy Installation',
          description: 'No professional help needed - install in minutes with our step-by-step instructions and included hardware.'
        },
        {
          icon: '🧪',
          title: 'Premium Materials',
          description: 'Built with high-grade, moisture-resistant materials that stand up to under-sink environments.'
        },
        {
          icon: '🔄',
          title: 'Smooth Sliding Mechanism',
          description: 'Our ball-bearing sliders ensure drawers open and close smoothly, even when fully loaded.'
        },
        {
          icon: '📏',
          title: 'Adjustable Design',
          description: 'Customize to fit your specific cabinet dimensions with our adaptable configuration options.'
        },
        {
          icon: '✨',
          title: 'Elegant Appearance',
          description: 'Clean, modern design that looks great while keeping your supplies neatly organized.'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* Section header animations - improved with better timing and easing */
.section-header {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.9s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: transform, opacity;
}

.section-header.visible {
  opacity: 1;
  transform: translateY(0);
}

.badge-animated, .title-animated, .description-animated {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.7s cubic-bezier(0.34, 1.56, 0.64, 1);
  will-change: transform, opacity;
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

/* Feature cards animations - enhanced with better timing */
.feature-card {
  opacity: 0;
  transform: translateY(40px);
  transition: all 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
  will-change: transform, opacity;
}

.feature-card.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Feature icon hover animation */
.feature-icon {
  transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
  box-shadow: 0 10px 25px -5px rgba(79, 70, 229, 0.1), 0 8px 10px -6px rgba(79, 70, 229, 0.1);
  will-change: transform;
}

.feature-card:hover .feature-icon {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 20px 25px -5px rgba(79, 70, 229, 0.2), 0 10px 10px -5px rgba(79, 70, 229, 0.2);
}

/* Text gradient effect */
.text-gradient {
  background: linear-gradient(90deg, #3B82F6, #10B981);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
}

/* Highlight feature animations */
.highlight-badge, .highlight-title, .highlight-description, .highlight-item, .highlight-image {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.7s cubic-bezier(0.34, 1.56, 0.64, 1);
  will-change: transform, opacity;
}

.highlight-badge.visible, .highlight-title.visible, .highlight-description.visible, .highlight-item.visible {
  opacity: 1;
  transform: translateY(0);
}

.highlight-image.visible {
  opacity: 1;
  transform: translateY(0);
}

.highlight-image-container {
  position: relative;
}

.highlight-image-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(59, 130, 246, 0.1), rgba(16, 185, 129, 0.1));
  z-index: 1;
  opacity: 0;
  transition: opacity 0.5s ease;
}

.highlight-image-container:hover::before {
  opacity: 1;
}

/* Float animations for decorative elements */
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
  100% { transform: translateY(0px); }
}

@keyframes pulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.3; }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

/* Floating animation for decorative elements */
.animate-float {
  animation: float 8s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 6s cubic-bezier(0.4, 0, 0.6, 1) infinite;
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

/* Special animations for the feature highlight section */
.features-grid {
  position: relative;
  z-index: 10;
}

/* Highlight feature animations */
.highlight-feature {
  position: relative;
  z-index: 10;
}

.highlight-badge, 
.highlight-title, 
.highlight-description, 
.highlight-item,
.highlight-image {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

.highlight-badge.visible,
.highlight-title.visible, 
.highlight-description.visible,
.highlight-item.visible {
  opacity: 1;
  transform: translateY(0);
}

.highlight-image {
  transform: scale(0.95) translateY(20px);
  filter: blur(5px);
  transition: all 1.2s cubic-bezier(0.5, 0, 0.1, 1);
}

.highlight-image.visible {
  opacity: 1;
  transform: scale(1) translateY(0);
  filter: blur(0);
}

.highlight-image-container {
  position: relative;
}

.highlight-image-container::before {
  content: '';
  position: absolute;
  top: -20px;
  right: -20px;
  width: 100px;
  height: 100px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.3) 0%, rgba(59, 130, 246, 0) 70%);
  border-radius: 50%;
  opacity: 0.6;
  animation: pulse-glow 4s infinite;
}

.highlight-image-container::after {
  content: '';
  position: absolute;
  bottom: -30px;
  left: -30px;
  width: 150px;
  height: 150px;
  background: radial-gradient(circle, rgba(16, 185, 129, 0.2) 0%, rgba(16, 185, 129, 0) 70%);
  border-radius: 50%;
  opacity: 0.5;
  animation: pulse-glow 5s infinite 1s;
}

@keyframes pulse-glow {
  0%, 100% { transform: scale(1); opacity: 0.5; }
  50% { transform: scale(1.1); opacity: 0.7; }
}

.highlight-icon {
  transition: all 0.3s ease;
}

.highlight-item:hover .highlight-icon {
  transform: scale(1.2) rotate(5deg);
  color: #10B981;
}
</style>
