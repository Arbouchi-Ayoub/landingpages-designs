<template>
    <div id="testimonials" class="py-5 bg-gray-50 dark:bg-gray-900 overflow-hidden relative">
      <!-- Decorative elements for visual interest -->
      <div class="hidden lg:block absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-blue-100 to-blue-200 dark:from-blue-900 dark:to-blue-800 rounded-full opacity-30 blur-3xl -z-10 animate-pulse-slow"></div>
      <div class="hidden lg:block absolute bottom-20 left-10 w-48 h-48 bg-gradient-to-tr from-blue-200 to-green-100 dark:from-blue-800 dark:to-green-900 rounded-full opacity-20 blur-3xl -z-10 animate-float"></div>
      
      <!-- Section content here -->
      <div class="container mx-auto px-4 md:px-6 relative z-10">
        <div class="text-center mb-16 reveal-section" :class="{'visible': isVisible}">
          <span class="inline-block py-1 px-3 rounded-full bg-blue-100 text-blue-800 dark:bg-blue-900 dark:text-blue-200 text-sm font-medium mb-4 reveal-item">TESTIMONIALS</span>
          <h2 class="text-3xl md:text-4xl font-bold mb-4 text-center text-gray-900 dark:text-white reveal-item">
            What Our <span class="text-gradient">Customers</span> Say
          </h2>
          <p class="max-w-2xl mx-auto text-lg text-gray-600 dark:text-gray-400 reveal-item">Don't just take our word for it - see what others think about our award-winning under-sink organizer.</p>
        </div>
        
        <!-- Testimonials grid with staggered animation -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 testimonials-container">
          <div 
            v-for="(testimonial, index) in testimonials" 
            :key="index" 
            class="testimonial-card bg-white dark:bg-gray-800 p-6 rounded-xl shadow-lg transform transition duration-500 hover:shadow-2xl hover:-translate-y-2 stagger-card"
            :class="{
              'visible': isVisible,
              'active': activeCard === index
            }"
            @mouseenter="setActiveCard(index)"
            @mouseleave="clearActiveCard"
          >
            <!-- Quote icon with animated background -->
            <div class="mb-4 relative">
              <div class="absolute -top-4 -left-4 w-12 h-12 rounded-full bg-blue-100 dark:bg-blue-900 opacity-30 transform transition-all duration-300 group-hover:scale-125"></div>
              <svg class="w-8 h-8 text-primary-600 dark:text-primary-400 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path>
              </svg>
            </div>

            <!-- Stars with animated glow -->
            <div class="flex mb-4 stars-container">
              <div v-for="i in 5" :key="i" class="text-yellow-400 transform transition duration-300 star-icon">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
                </svg>
              </div>
            </div>

            <!-- Quote with animated appear effect -->
            <div class="relative">
              <p class="text-gray-600 dark:text-gray-300 italic mb-6 testimonial-quote">
                "{{ testimonial.quote }}"
              </p>
            </div>

            <!-- Customer info with animated photo -->
            <div class="flex items-center mt-6 pt-4 border-t border-gray-100 dark:border-gray-700">
              <div class="relative mr-4 overflow-hidden rounded-full ring-2 ring-primary-500 dark:ring-primary-400 p-0.5 transform transition duration-500 hover:scale-110">
                <img 
                  :src="testimonial.avatar" 
                  alt="Customer photo" 
                  class="w-12 h-12 rounded-full object-cover"
                  :class="{'pulse-glow': activeCard === index}"
                />
              </div>
              <div>
                <p class="font-medium text-gray-900 dark:text-white">{{ testimonial.name }}</p>
                <p class="text-sm text-gray-500 dark:text-gray-400 flex items-center">
                  <svg class="w-4 h-4 mr-1 text-primary-500" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"></path>
                  </svg>
                  {{ testimonial.location }}
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial navigation indicators -->
        <div class="flex justify-center mt-10 space-x-2">
          <button 
            v-for="(_, index) in testimonials" 
            :key="'nav-' + index"
            class="w-3 h-3 rounded-full transition-all duration-300 focus:outline-none"
            :class="activeCard === index ? 'bg-primary-500 dark:bg-primary-400 scale-125' : 'bg-gray-300 dark:bg-gray-700'"
            @click="setActiveCard(index)"
          ></button>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  name: 'TestimonialsSection',
  setup() {
    const isVisible = ref(false);
    const activeCard = ref(null);
    let autoplayInterval = null;
    
    const setActiveCard = (index) => {
      activeCard.value = index;
      // Reset autoplay timer when manually selecting a card
      if (autoplayInterval) {
        clearInterval(autoplayInterval);
        startAutoplay();
      }
    };
    
    const clearActiveCard = () => {
      // Don't clear during autoplay
      if (!autoplayInterval) {
        activeCard.value = null;
      }
    };
    
    // Automatic card cycling
    const startAutoplay = () => {
      autoplayInterval = setInterval(() => {
        const testimonials = 3; // Match the length of your testimonials array
        activeCard.value = (activeCard.value === null) ? 0 : (activeCard.value + 1) % testimonials;
      }, 3000);
    };
    
    // Setup animation triggers when section becomes visible
    onMounted(() => {
      const testimonialSection = document.getElementById('testimonials');
      if (testimonialSection) {
        const stop = useIntersectionObserver(
          testimonialSection,
          ([{ isIntersecting }]) => {
            if (isIntersecting) {
              isVisible.value = true;
              // Add visible class to testimonial cards
              document.querySelectorAll('.stagger-card').forEach(card => {
                card.classList.add('visible');
              });
              // Start autoplay when section is visible
              startAutoplay();
              // Stop observing once triggered
              stop();
            }
          },
          { threshold: 0.2 }
        );
      }
    });
    
    // Cleanup on component unmount
    onBeforeUnmount(() => {
      if (autoplayInterval) {
        clearInterval(autoplayInterval);
      }
    });
    
    return {
      isVisible,
      activeCard,
      setActiveCard,
      clearActiveCard
    };
  },
  data() {
    return {
      testimonials: [
        {
          name: 'Sarah Johnson',
          location: 'New York, NY',
          avatar: 'https://randomuser.me/api/portraits/women/32.jpg',
          quote: 'This organizer completely transformed my under-sink area. Everything is easily accessible now, and it looks so much cleaner!'
        },
        {
          name: 'Michael Roberts',
          location: 'Chicago, IL',
          avatar: 'https://randomuser.me/api/portraits/men/46.jpg',
          quote: 'I was skeptical at first, but this organizer is sturdy and fits perfectly around my plumbing. No more searching for cleaning supplies!'
        },
        {
          name: 'Emily Chen',
          location: 'San Francisco, CA',
          avatar: 'https://randomuser.me/api/portraits/women/26.jpg',
          quote: 'The adjustable width feature is genius! I\'ve tried several organizers before, but this is the only one that actually works with my sink configuration.'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* Section reveal animation */
.reveal-section {
  opacity: 0;
  transform: translateY(30px);
  transition: all 1s cubic-bezier(0.5, 0, 0.1, 1);
}

.reveal-section.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Staggered animation for reveal items */
.reveal-item {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

.reveal-section.visible .reveal-item {
  opacity: 1;
  transform: translateY(0);
}

.reveal-section.visible .reveal-item:nth-child(1) {
  transition-delay: 0.1s;
}

.reveal-section.visible .reveal-item:nth-child(2) {
  transition-delay: 0.3s;
}

.reveal-section.visible .reveal-item:nth-child(3) {
  transition-delay: 0.5s;
}

/* Testimonial cards staggered animation */
.testimonials-container {
  perspective: 1000px;
}

.stagger-card {
  opacity: 0;
  transform: translateY(40px) scale(0.95);
  transition: all 0.6s cubic-bezier(0.5, 0, 0.1, 1), box-shadow 0.3s ease, transform 0.3s ease;
  will-change: transform, opacity;
}

.stagger-card.visible {
  opacity: 1;
  transform: translateY(0) scale(1);
}

/* Stagger the cards appearance */
.stagger-card:nth-child(1) {
  transition-delay: 0.1s;
}

.stagger-card:nth-child(2) {
  transition-delay: 0.25s;
}

.stagger-card:nth-child(3) {
  transition-delay: 0.4s;
}

/* Highlight active card */
.testimonial-card.active {
  background: linear-gradient(145deg, #ffffff, #f0f9ff);
  box-shadow: 0 10px 25px -5px rgba(59, 130, 246, 0.1), 0 8px 10px -6px rgba(59, 130, 246, 0.1);
  transform: translateY(-8px);
}

.dark .testimonial-card.active {
  background: linear-gradient(145deg, #1f2937, #111827);
}

/* Stars animation */
.stars-container {
  display: flex;
  gap: 2px;
}

.star-icon {
  transition: transform 0.3s ease;
}

.active .star-icon:hover {
  transform: scale(1.2) rotate(5deg);
  filter: drop-shadow(0 0 3px rgba(250, 204, 21, 0.7));
}

/* Quote animation */
.testimonial-quote {
  position: relative;
  transition: transform 0.3s ease;
}

.active .testimonial-quote {
  transform: scale(1.02);
}

.testimonial-quote::before,
.testimonial-quote::after {
  content: '"';
  font-size: 2rem;
  line-height: 0.5;
  color: #cbd5e1;
}

.dark .testimonial-quote::before,
.dark .testimonial-quote::after {
  color: #475569;
}

.testimonial-quote::before {
  position: absolute;
  left: -10px;
  top: 0;
}

.testimonial-quote::after {
  position: absolute;
  bottom: -10px;
  right: -10px;
}

/* Gradient text effect */
.text-gradient {
  background: linear-gradient(90deg, #3B82F6, #10B981);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
}

/* Glow effect for active testimonial photos */
.pulse-glow {
  animation: pulse-glow 2s infinite;
}

@keyframes pulse-glow {
  0% {
    box-shadow: 0 0 0 0 rgba(59, 130, 246, 0.4);
  }
  70% {
    box-shadow: 0 0 0 10px rgba(59, 130, 246, 0);
  }
  100% {
    box-shadow: 0 0 0 0 rgba(59, 130, 246, 0);
  }
}

/* Floating animation for decorative elements */
.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse-slow 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0px); }
}

@keyframes pulse-slow {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.15; transform: scale(1.1); }
}
</style>