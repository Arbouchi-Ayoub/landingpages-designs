<template>
  <div id="specifications" class="bg-white dark:bg-gray-900 overflow-hidden">
    <div class="container mx-auto px-4 md:px-6 relative">
      <!-- Enhanced decorative elements for visual interest -->
      <div class="hidden lg:block absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-blue-100 to-blue-200 dark:from-blue-900 dark:to-blue-800 rounded-full opacity-30 blur-3xl -z-10 animate-pulse-slow"></div>
      <div class="hidden lg:block absolute bottom-20 left-10 w-48 h-48 bg-gradient-to-tr from-blue-200 to-green-100 dark:from-blue-800 dark:to-green-900 rounded-full opacity-20 blur-3xl -z-10 animate-float"></div>
      <div class="hidden lg:block absolute top-40 left-0 w-32 h-32 bg-gradient-to-tl from-purple-100 to-pink-200 dark:from-purple-900 dark:to-pink-900 rounded-full opacity-20 blur-2xl -z-10" style="animation: float 7s ease-in-out infinite alternate; animation-delay: 1s;"></div>
      <div class="hidden lg:block absolute bottom-40 right-20 w-24 h-24 bg-gradient-to-br from-green-100 to-cyan-200 dark:from-green-900 dark:to-cyan-900 rounded-full opacity-15 blur-xl -z-10" style="animation: float 5s ease-in-out infinite alternate-reverse; animation-delay: 2s;"></div>
      
      <!-- Section Header with animation -->
      <div class="max-w-3xl mx-auto text-center mb-16 reveal">
        <div class="inline-block px-3 py-1 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 text-sm font-medium rounded-full mb-4 transform transition hover:scale-105 hover:shadow-md">
          <span class="flex items-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-1 animate-spin-slow" viewBox="0 0 20 20" fill="currentColor">
              <path fill-rule="evenodd" d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z" clip-rule="evenodd" />
            </svg>
            Premium Quality
          </span>
        </div>
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 dark:text-white bg-clip-text text-transparent bg-gradient-to-r from-gray-900 to-gray-600 dark:from-white dark:to-gray-300">
          Product Specifications & Pricing
        </h2>
        <p class="text-lg text-gray-600 dark:text-gray-400">
          Engineered with premium materials and thoughtful design for years of reliable use
        </p>
      </div>
      
      <!-- Main Content Area -->
      <div class="flex flex-col lg:flex-row gap-10">
        <!-- Specifications Column with staggered animation -->
        <div class="lg:w-1/2 reveal">
          <div class="bg-gray-50 dark:bg-gray-800 rounded-2xl overflow-hidden shadow-lg border border-gray-200 dark:border-gray-700 transform transition duration-500 hover:shadow-2xl">
            <div class="p-8">
              <div class="flex items-center mb-8">
                <div class="w-12 h-12 flex-shrink-0 rounded-full bg-blue-100 dark:bg-blue-900 flex items-center justify-center shadow-md transform transition-transform hover:scale-110 hover:rotate-12">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-600 dark:text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z" />
                  </svg>
                </div>
                <h3 class="ml-4 text-2xl font-bold text-gray-900 dark:text-white bg-clip-text text-transparent bg-gradient-to-r from-blue-600 to-blue-400 dark:from-blue-400 dark:to-blue-200">Technical Specifications</h3>
              </div>
              
              <!-- Specs List with interactive elements -->
              <div class="space-y-8 mb-8 stagger-reveal">
                <div 
                  v-for="(spec, index) in specifications" 
                  :key="index" 
                  class="group transform transition duration-500 hover:-translate-y-1"
                  @mouseenter="highlightSpec(index)"
                  @mouseleave="resetHighlight()"
                >
                  <div class="flex justify-between items-center mb-3">
                    <span class="font-semibold text-gray-900 dark:text-white group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors flex items-center">
                      <span class="inline-block w-6 h-6 rounded-full bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 flex items-center justify-center mr-2 text-xs font-bold">{{index + 1}}</span>
                      {{ spec.name }}
                    </span>
                    <span 
                      class="px-3 py-1 text-xs font-medium rounded-full transition-all duration-300 transform group-hover:scale-110" 
                      :class="spec.highlight ? 'bg-blue-100 text-blue-700 dark:bg-blue-900 dark:text-blue-300' : 'bg-gray-100 text-gray-700 dark:bg-gray-700 dark:text-gray-300'"
                    >
                      {{ spec.highlight ? 'Premium Feature' : 'Standard' }}
                    </span>
                  </div>
                  <div class="flex items-center">
                    <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-3 overflow-hidden">
                      <div 
                        class="h-3 rounded-full transition-all duration-1000 relative"
                        :class="{
                          'bg-gradient-to-r from-blue-500 to-blue-700 dark:from-blue-400 dark:to-blue-600': spec.highlight,
                          'bg-gradient-to-r from-gray-400 to-gray-500 dark:from-gray-500 dark:to-gray-600': !spec.highlight,
                          'animate-pulse': activeSpecIndex === index
                        }" 
                        :style="{ width: (activeSpecIndex === index ? '100%' : spec.quality + '%') }"
                      >
                        <div v-if="activeSpecIndex === index" class="absolute top-0 right-0 h-full w-8 bg-gradient-to-r from-transparent to-white dark:to-gray-300 opacity-30 animate-shimmer"></div>
                      </div>
                    </div>
                    <span class="ml-3 min-w-[80px] text-sm text-gray-600 dark:text-gray-400 font-medium">{{ spec.value }}</span>
                  </div>
                </div>
              </div>
              
              <!-- Materials & Certification with hover effects -->
              <div class="bg-gradient-to-br from-gray-100 to-gray-200 dark:from-gray-700 dark:to-gray-800 p-6 rounded-xl hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1 relative overflow-hidden group">
                <!-- Decorative element -->
                <div class="absolute -right-10 -top-10 w-20 h-20 bg-blue-100 dark:bg-blue-900 rounded-full opacity-30 group-hover:scale-150 transition-transform duration-500"></div>
                
                <div class="relative z-10">
                  <h4 class="font-bold text-lg mb-4 text-gray-900 dark:text-white flex items-center">
                    <svg class="h-6 w-6 mr-2 text-blue-600 dark:text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                    </svg>
                    Materials & Certification
                  </h4>
                  <ul class="space-y-3">
                    <li class="flex items-center p-2 hover:bg-white hover:dark:bg-gray-700 rounded-lg transition-colors duration-200 group cursor-pointer">
                      <svg class="h-5 w-5 mr-3 text-green-500 group-hover:scale-125 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                      <span class="text-gray-700 dark:text-gray-300 group-hover:text-gray-900 group-hover:dark:text-white transition-colors duration-200">BPA-free ABS plastic construction</span>
                    </li>
                    <li class="flex items-center p-2 hover:bg-white hover:dark:bg-gray-700 rounded-lg transition-colors duration-200 group cursor-pointer">
                      <svg class="h-5 w-5 mr-3 text-green-500 group-hover:scale-125 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                      <span class="text-gray-700 dark:text-gray-300 group-hover:text-gray-900 group-hover:dark:text-white transition-colors duration-200">Stainless steel sliding mechanisms</span>
                    </li>
                    <li class="flex items-center p-2 hover:bg-white hover:dark:bg-gray-700 rounded-lg transition-colors duration-200 group cursor-pointer">
                      <svg class="h-5 w-5 mr-3 text-green-500 group-hover:scale-125 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                      <span class="text-gray-700 dark:text-gray-300 group-hover:text-gray-900 group-hover:dark:text-white transition-colors duration-200">FDA & EU certified materials</span>
                    </li>
                    <li class="flex items-center p-2 hover:bg-white hover:dark:bg-gray-700 rounded-lg transition-colors duration-200 group cursor-pointer">
                      <svg class="h-5 w-5 mr-3 text-green-500 group-hover:scale-125 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                      <span class="text-gray-700 dark:text-gray-300 group-hover:text-gray-900 group-hover:dark:text-white transition-colors duration-200">Eco-friendly recyclable packaging</span>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Pricing Column -->
        <div class="lg:w-1/2 reveal">
          <div class="relative bg-white dark:bg-gray-800 rounded-2xl overflow-hidden shadow-xl border border-gray-200 dark:border-gray-700 transform transition-all duration-500 hover:shadow-2xl hover:scale-[1.02] group">
            <!-- Animated decorative elements -->
            <div class="absolute -left-10 -top-10 w-40 h-40 bg-gradient-to-br from-primary-100 to-primary-200 dark:from-primary-900 dark:to-primary-800 rounded-full opacity-20 blur-xl transition-all duration-700 group-hover:opacity-30 group-hover:scale-110"></div>
            <div class="absolute -right-20 -bottom-20 w-60 h-60 bg-gradient-to-tl from-blue-100 to-green-100 dark:from-blue-900 dark:to-green-900 rounded-full opacity-10 blur-2xl transition-all duration-700 group-hover:opacity-20 group-hover:scale-110"></div>
            
            <!-- Popular Badge with animation -->
            <div class="absolute top-6 right-6 z-10 animate-pulse-slow">
              <span class="inline-flex items-center px-4 py-2 rounded-full text-xs font-bold bg-gradient-to-r from-primary-600 to-primary-400 dark:from-primary-500 dark:to-primary-400 text-white shadow-md transform transition-transform hover:scale-110">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z" />
                </svg>
                Most Popular
              </span>
            </div>
            
            <!-- Pricing Header with animations -->
            <div class="relative z-10 pt-10 pb-8 px-8 border-b border-gray-200 dark:border-gray-700 stagger-reveal">
              <div class="flex justify-between items-center mb-3">
                <h3 class="text-2xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-primary-600 to-primary-400 dark:from-primary-400 dark:to-primary-200">Premium Package</h3>
                <div class="px-3 py-1 text-sm font-bold text-white bg-gradient-to-r from-green-500 to-green-400 rounded-full shadow-sm transform transition hover:scale-110 hover:shadow">
                  Save 25%
                </div>
              </div>
              <div class="mt-5 flex items-baseline">
                <span class="text-4xl md:text-5xl font-extrabold text-gray-900 dark:text-white">$34.99</span>
                <span class="ml-1 text-xl font-medium text-gray-500 dark:text-gray-400">USD</span>
                <span class="ml-3 text-lg line-through text-gray-500 dark:text-gray-400">$46.99</span>
              </div>
              <p class="mt-3 text-sm text-gray-500 dark:text-gray-400 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 mr-1 text-green-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                One-time purchase, free shipping
              </p>
            </div>
            
            <!-- Features List with animations -->
            <div class="relative z-10 pt-6 pb-8 px-8">
              <p class="text-sm font-bold text-gray-900 dark:text-gray-100 uppercase tracking-wider mb-5 flex items-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-500 mr-2" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                </svg>
                What's Included
              </p>
              <ul class="space-y-4 stagger-reveal">
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0 transition transform duration-300 group-hover:scale-125" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Premium Under-Sink Organizer</span>
                </li>
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Adjustable Width: 20-24 inches</span>
                </li>
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">2 Sliding Drawers with Dividers</span>
                </li>
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300">Installation Hardware & Manual</span>
                </li>
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><span class="font-semibold text-gray-900 dark:text-white">2-Year</span> Manufacturer's Warranty</span>
                </li>
                <li class="flex items-start p-2 rounded-lg transition-colors duration-200 hover:bg-gray-50 dark:hover:bg-gray-700">
                  <svg class="h-5 w-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  <span class="text-gray-700 dark:text-gray-300"><span class="font-semibold text-gray-900 dark:text-white">30-Day</span> Money-Back Guarantee</span>
                </li>
              </ul>
            </div>
            
            <!-- CTA Button with animation -->
            <div class="px-8 py-6 relative z-10">
              <button 
                class="w-full py-4 px-8 bg-gradient-to-r from-primary-600 to-primary-500 hover:from-primary-700 hover:to-primary-600 text-white text-lg font-bold rounded-lg shadow-lg hover:shadow-xl transform transition duration-300 hover:-translate-y-1 flex items-center justify-center relative overflow-hidden group"
                @mouseover="animateButtonShimmer"
                @click="addToCart"
              >
                <!-- Button shimmer effect -->
                <span ref="buttonShimmer" class="absolute inset-0 w-full h-full bg-gradient-to-r from-transparent via-white to-transparent opacity-30 -translate-x-full shimmer-effect"></span>
                
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
                Add to Cart
              </button>
              <p class="text-center text-sm text-gray-500 dark:text-gray-400 mt-2">Free shipping on all orders</p>
            </div>
            
            <!-- Satisfaction Guarantee -->
            <div class="bg-gray-50 dark:bg-gray-900 px-8 py-6 border-t border-gray-200 dark:border-gray-700 relative overflow-hidden reveal">
              <!-- Decorative elements -->
              <div class="absolute -left-10 -bottom-10 w-32 h-32 bg-primary-100 dark:bg-primary-900 rounded-full opacity-10 blur-xl animate-float"></div>
              <div class="absolute right-10 top-0 w-16 h-16 bg-green-100 dark:bg-green-900 rounded-full opacity-20 blur-lg animate-float" style="animation-delay: 1s;"></div>
              
              <div class="flex items-center relative z-10">
                <div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-green-400 to-green-500 dark:from-green-500 dark:to-green-600 rounded-full flex items-center justify-center shadow-md transform transition-transform hover:scale-110 hover:rotate-6">
                  <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                  </svg>
                </div>
                <div class="ml-4">
                  <h5 class="font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-600 to-green-400 dark:from-green-400 dark:to-green-300 mb-1 text-lg">100% Satisfaction Guarantee</h5>
                  <p class="text-sm text-gray-600 dark:text-gray-400">Not happy with your purchase? Return within 30 days for a full refund, no questions asked.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, nextTick } from 'vue';
import { useIntersectionObserver } from '@vueuse/core';

export default {
  data() {
    return {
      specifications: [
        {
          name: 'Build Quality',
          quality: 95,
          value: 'Excellent',
          highlight: true
        },
        {
          name: 'Material Durability',
          quality: 90,
          value: 'Very Good',
          highlight: true
        },
        {
          name: 'Space Efficiency',
          quality: 100,
          value: 'Outstanding',
          highlight: true
        },
        {
          name: 'Ease of Installation',
          quality: 85,
          value: 'Good',
          highlight: false
        },
        {
          name: 'Adjustability',
          quality: 95,
          value: 'Excellent',
          highlight: true
        },
        {
          name: 'Cleaning Ease',
          quality: 80,
          value: 'Good',
          highlight: false
        }
      ],
      packageFeatures: [
        'Premium Under-Sink Organizer',
        'Adjustable Width: 20-24 inches',
        '2 Sliding Drawers with Dividers',
        'Installation Hardware & Manual',
        "2-Year Manufacturer's Warranty",
        '30-Day Money-Back Guarantee'
      ],
      activeSpecIndex: null,
      sectionVisible: false,
      animationComplete: false,
      buttonShimmerActive: false
    };
  },
  methods: {
    highlightSpec(index) {
      this.activeSpecIndex = index;
    },
    resetHighlight() {
      this.activeSpecIndex = null;
    },
    animateButtonShimmer() {
      // Prevent multiple animations from triggering at once
      if (this.buttonShimmerActive) return;
      
      this.buttonShimmerActive = true;
      const shimmerElement = this.$refs.buttonShimmer;
      
      if (shimmerElement) {
        shimmerElement.classList.add('animate-shimmer');
        
        setTimeout(() => {
          shimmerElement.classList.remove('animate-shimmer');
          this.buttonShimmerActive = false;
        }, 1000);
      } else {
        this.buttonShimmerActive = false;
      }
    },
    addToCart() {
      // This would typically integrate with your shopping cart system
      alert('Product added to cart!');
    },
    setupAnimations() {
      // Set up intersection observer for the reveal animations using VueUse
      const specSection = document.querySelector('#specifications');
      
      if (specSection) {
        const stop = useIntersectionObserver(
          specSection,
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
      
      // Add staggered animation to all elements with stagger-reveal class
      const staggerElements = document.querySelectorAll('.stagger-reveal');
      staggerElements.forEach((container) => {
        const children = Array.from(container.children);
        children.forEach((el, i) => {
          setTimeout(() => {
            el.classList.add('fade-in');
          }, 300 + (i * 100));
        });
      });
      
      setTimeout(() => {
        this.animationComplete = true;
      }, 1500);
    }
  },
  mounted() {
    this.setupAnimations();
  }
};
</script>

<style scoped>
.section-visible {
  opacity: 1;
  transform: translateY(0);
}

.reveal {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.8s ease-out;
}

.stagger-reveal > * {
  opacity: 0;
  transform: translateY(15px);
  transition: all 0.5s ease-out;
}

.stagger-reveal > *.fade-in {
  opacity: 1;
  transform: translateY(0);
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.animate-shimmer {
  animation: shimmer 2s infinite;
}

.shimmer-effect.animate-shimmer {
  animation: shimmer 1s forwards;
}

@keyframes shimmer-once {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.group-hover\:animate-shimmer-once:hover {
  animation: shimmer-once 1s;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-spin-slow {
  animation: spin 8s linear infinite;
}

.animate-pulse-slow {
  animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
</style>

<style scoped>
.btn-primary {
  @apply inline-flex items-center justify-center px-6 bg-primary-600 dark:bg-primary-700 text-white font-medium rounded-lg hover:bg-primary-700 dark:hover:bg-primary-600 transition duration-300 ease-in-out;
}
</style>
