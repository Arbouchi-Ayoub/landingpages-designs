<template>
  <div id="faq-section" class="bg-gray-50 dark:bg-gray-800 relative overflow-hidden">
    <!-- Decorative elements for visual interest -->
    <div class="hidden lg:block absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-purple-100 to-indigo-100 dark:from-purple-900 dark:to-indigo-900 rounded-full opacity-30 blur-3xl -z-10 animate-pulse-slow"></div>
    <div class="hidden lg:block absolute bottom-20 left-10 w-48 h-48 bg-gradient-to-tr from-blue-100 to-primary-100 dark:from-blue-900 dark:to-primary-900 rounded-full opacity-20 blur-3xl -z-10 animate-float"></div>
    <div class="hidden lg:block absolute top-40 left-0 w-32 h-32 bg-gradient-to-tl from-green-100 to-teal-100 dark:from-green-900 dark:to-teal-900 rounded-full opacity-20 blur-2xl -z-10" style="animation: float 8s ease-in-out infinite alternate; animation-delay: 1s;"></div>
    
    <div class="container mx-auto px-4 md:px-6 py-6 relative z-10">
      <div class="max-w-3xl mx-auto text-center mb-16 reveal">
        <div class="inline-block px-3 py-1 bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 text-sm font-medium rounded-full mb-4 transform transition hover:scale-105 hover:shadow-md opacity-100">
          Questions & Answers
        </div>
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 dark:text-white opacity-100">
          Frequently Asked <span class="text-gradient-primary">Questions</span>
        </h2>
        <p class="text-lg text-gray-600 dark:text-gray-400 max-w-3xl mx-auto opacity-100">
          Get answers to the most common questions about our under-sink organizer.
        </p>
      </div>
    </div>
    <div class="max-w-3xl mx-auto faq-container">
      <div 
        v-for="(item, index) in faqItems" 
        :key="index" 
        class="mb-6 bg-white dark:bg-gray-900 rounded-xl shadow-sm hover:shadow-md border border-gray-100 dark:border-gray-700 transition-all duration-300 overflow-hidden faq-item"
        :class="{'shadow-md': openIndex === index}"
        :style="{ transitionDelay: `${index * 50}ms` }"
      >
        <button 
          @click="toggleFaq(index)" 
          class="flex justify-between items-center w-full text-left p-6 focus:outline-none group"
        >
          <h3 class="text-xl font-medium text-gray-900 dark:text-white group-hover:text-primary-600 dark:group-hover:text-primary-400 transition-colors duration-300 flex items-center">
            <span class="inline-flex items-center justify-center w-8 h-8 rounded-full bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 mr-3 text-sm font-bold">{{ index + 1 }}</span>
            {{ item.question }}
          </h3>
          <div class="w-10 h-10 flex items-center justify-center rounded-full bg-gray-100 dark:bg-gray-800 group-hover:bg-primary-100 dark:group-hover:bg-primary-900 transition-all duration-300">
            <svg 
              class="w-5 h-5 text-gray-500 dark:text-gray-400 group-hover:text-primary-600 dark:group-hover:text-primary-400 transform transition-transform duration-300" 
              :class="{ 'rotate-180': openIndex === index }"
              fill="none" 
              stroke="currentColor" 
              viewBox="0 0 24 24" 
              xmlns="http://www.w3.org/2000/svg"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
            </svg>
          </div>
        </button>
        
        <div 
          class="overflow-hidden transition-all duration-300 answer-container"
          :class="{ 'max-h-0': openIndex !== index, 'max-h-96': openIndex === index }"
        >
          <div class="p-6 pt-0 border-t border-gray-100 dark:border-gray-700">
            <p class="text-gray-600 dark:text-gray-300">{{ item.answer }}</p>
          </div>
        </div>
      </div>
    </div>
    
    <div class="mt-12 text-center cta-section">
      <p class="text-gray-700 dark:text-gray-300 mb-6">Still have questions about our products?</p>
      <a href="#contact" class="inline-flex items-center justify-center px-6 py-3 bg-gradient-to-r from-primary-600 to-primary-500 hover:from-primary-700 hover:to-primary-600 text-white font-medium rounded-lg shadow-md hover:shadow-lg transform transition duration-300 hover:-translate-y-1 hover:scale-[1.02]">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
        </svg>
        Contact Our Support Team
      </a>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  name: 'FaqSection',
  setup() {
    const isVisible = ref(false);
    
    onMounted(() => {
      // Items are now visible by default, no need for complex animations
      isVisible.value = true;
    });
    
    return {
      isVisible
    };
  },
  data() {
    return {
      openIndex: 0, // First FAQ item open by default
      faqItems: [
        {
          question: "What are the dimensions of the organizer?",
          answer: "The OrganizeMax Under-Sink Organizer has adjustable width from 20-24 inches, depth of 12 inches, and height of 15 inches. The adjustable design allows it to fit most standard under-sink cabinets."
        },
        {
          question: "How difficult is the installation?",
          answer: "Installation is very straightforward and typically takes 10-15 minutes. All necessary hardware is included, along with step-by-step instructions. No special tools are required, just a standard screwdriver."
        },
        {
          question: "Will it work with my plumbing?",
          answer: "Yes! Our organizer is designed to work around standard under-sink plumbing. The adjustable design allows you to customize the fit around pipes and garbage disposals."
        },
        {
          question: "What materials is it made from?",
          answer: "The OrganizeMax Under-Sink Organizer is constructed from high-grade ABS plastic with stainless steel rails. These materials are chosen for durability and moisture resistance in under-sink environments."
        },
        {
          question: "How much weight can it hold?",
          answer: "Each drawer can safely hold up to 30 pounds of items, which is more than enough for most cleaning supplies, kitchen items, or bathroom products."
        },
        {
          question: "Do you offer a warranty?",
          answer: "Yes, all OrganizeMax Under-Sink Organizers come with a 2-year manufacturer warranty against defects. We also offer a 30-day money-back guarantee if you're not completely satisfied."
        }
      ]
    }
  },
  methods: {
    toggleFaq(index) {
      // Toggle the FAQ item open/closed state
      this.openIndex = this.openIndex === index ? null : index;
      
      // Add small delay to allow animation to complete before scrolling into view
      if (this.openIndex === index) {
        setTimeout(() => {
          const element = document.querySelectorAll('.faq-item')[index];
          if (element) {
            element.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
          }
        }, 100);
      }
    }
  }
}
</script>

<style scoped>
/* Section header animations */
.reveal {
  opacity: 1;
  transition: all 0.9s cubic-bezier(0.16, 1, 0.3, 1);
}

/* FAQ item animations */
.faq-item {
  opacity: 1;
  transition: all 0.6s cubic-bezier(0.5, 0, 0.1, 1);
  will-change: transform, opacity, max-height; /* Performance optimization */
}

/* Fix max-height transition for FAQ accordion */
.answer-container {
  will-change: max-height;
  transition: max-height 0.4s cubic-bezier(0.5, 0, 0.1, 1);
}

.max-h-0 {
  max-height: 0;
  overflow: hidden;
}

.max-h-96 {
  max-height: 400px; /* Ensure enough space for larger answers */
}

/* CTA section animations */
.cta-section {
  opacity: 1;
  transition: all 0.8s cubic-bezier(0.5, 0, 0.1, 1);
}

/* Text gradient effect */
.text-gradient-primary {
  background: linear-gradient(90deg, #4F46E5, #818CF8);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
}

/* Animations for decorative elements */
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
  100% { transform: translateY(0px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-pulse-slow {
  animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}
</style>
