<template>
  <!-- Navigation Bar with Logo - Enhanced with glass morphism and animations -->
  <header class="header-animated absolute top-0 left-0 w-full z-10 py-4 transition-all duration-500 bg-white bg-opacity-90 dark:bg-gray-900 dark:bg-opacity-90 backdrop-filter backdrop-blur-md shadow-lg">
    <div class="container mx-auto px-4 md:px-6">
      <nav class="flex justify-between items-center">
        <div class="flex items-center">
          <div class="text-primary-600 dark:text-primary-400 text-2xl font-bold flex items-center logo-animated">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mr-2 logo-icon" viewBox="0 0 24 24" fill="currentColor">
              <path d="M21,4H3C2.447,4,2,4.448,2,5v14c0,0.552,0.447,1,1,1h18c0.553,0,1-0.448,1-1V5C22,4.448,21.553,4,21,4z M8,18H4v-5h4V18z M14,18h-4v-5h4V18z M14,11H4V6h10V11z M20,18h-4v-5h4V18z M20,11h-4V6h4V11z"/>
            </svg>
            <span>OrganizeMax</span>
          </div>
        </div>
        <!-- Desktop Navigation Menu with hover animations -->
        <div class="hidden md:flex space-x-8 text-sm font-medium nav-links">
          <a href="#features" class="nav-link text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors relative">Features</a>
          <a href="#benefits" class="nav-link text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors relative">Benefits</a>
          <a href="#specs" class="nav-link text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors relative">Specifications</a>
          <a href="#reviews" class="nav-link text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors relative">Reviews</a>
          <a href="#faq" class="nav-link text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors relative">FAQ</a>
        </div>
        <div class="flex items-center space-x-4">
          <!-- Dark/Light Mode Toggle -->
          <button 
            @click="toggleDarkMode" 
            class="p-2 rounded-full text-gray-700 hover:bg-gray-100 dark:text-gray-300 dark:hover:bg-gray-800 transition-colors focus:outline-none"
            aria-label="Toggle dark/light mode"
          >
            <!-- Sun icon for dark mode (show when in dark mode) -->
            <svg 
              v-if="isDarkMode" 
              xmlns="http://www.w3.org/2000/svg" 
              class="h-5 w-5" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path 
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" 
              />
            </svg>
            <!-- Moon icon for light mode (show when in light mode) -->
            <svg 
              v-else
              xmlns="http://www.w3.org/2000/svg" 
              class="h-5 w-5" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path 
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" 
              />
            </svg>
          </button>

          <button class="btn-animated bg-primary-600 hover:bg-primary-700 text-white px-4 py-2 rounded-md text-sm font-medium transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg relative overflow-hidden">
            Buy Now
          </button>
          
          <!-- Mobile Menu Toggle Button -->
          <button 
            @click="toggleMobileMenu" 
            class="text-gray-700 dark:text-white md:hidden focus:outline-none"
            aria-label="Toggle mobile menu"
          >
            <!-- Hamburger icon when menu is closed -->
            <svg 
              v-if="!mobileMenuOpen"
              xmlns="http://www.w3.org/2000/svg" 
              class="h-6 w-6" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <!-- X icon when menu is open -->
            <svg 
              v-else
              xmlns="http://www.w3.org/2000/svg" 
              class="h-6 w-6" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </nav>

      <!-- Mobile Menu (hidden by default) -->
      <div 
        v-show="mobileMenuOpen" 
        class="md:hidden mt-4 py-4 border-t border-gray-200 dark:border-gray-700 transition-all duration-300"
      >
        <div class="flex flex-col space-y-4 text-sm font-medium">
          <a href="#features" class="text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors py-2">Features</a>
          <a href="#benefits" class="text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors py-2">Benefits</a>
          <a href="#specs" class="text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors py-2">Specifications</a>
          <a href="#reviews" class="text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors py-2">Reviews</a>
          <a href="#faq" class="text-gray-700 hover:text-primary-600 dark:text-gray-300 dark:hover:text-primary-400 transition-colors py-2">FAQ</a>
        </div>
      </div>
    </div>
  </header>

  <!-- Hero Section - Enhanced with animations and interactive elements -->
  <div class="pt-24 pb-16 md:pt-32 md:pb-24 bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800 relative overflow-hidden">
    <!-- Decorative animated shapes -->
    <div class="absolute top-20 left-0 w-64 h-64 bg-primary-100 dark:bg-primary-900 rounded-full mix-blend-multiply filter blur-3xl opacity-30 animate-blob"></div>
    <div class="absolute top-40 right-10 w-72 h-72 bg-blue-100 dark:bg-blue-900 rounded-full mix-blend-multiply filter blur-3xl opacity-30 animate-blob animation-delay-2000"></div>
    <div class="absolute -bottom-8 left-20 w-56 h-56 bg-green-100 dark:bg-green-900 rounded-full mix-blend-multiply filter blur-3xl opacity-30 animate-blob animation-delay-4000"></div>
    
    <div class="container mx-auto px-4 md:px-6 relative z-10">
      <div class="flex flex-col md:flex-row items-center gap-8 md:gap-12">
        <div class="md:w-1/2 md:pr-8 hero-content">
          <div class="mb-4 inline-block px-3 py-1 rounded-full bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-400 text-sm font-medium badge-animated">
            #1 Best Seller in Cabinet Organizers
          </div>
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-4 text-gray-900 dark:text-white leading-tight hero-title">
            <span class="gradient-text">Transform Your</span> <span class="text-primary-600 dark:text-primary-400">Under-Sink</span> Space
          </h1>
          <p class="text-lg text-gray-600 dark:text-gray-300 mb-6 hero-description">
            Our premium sliding drawer organizer brings efficiency to your kitchen or bathroom with expandable, adjustable storage that maximizes every inch of your cabinet space.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 mb-8">
            <button class="bg-primary-600 hover:bg-primary-700 text-white px-6 py-4 rounded-lg font-medium flex items-center justify-center transition duration-300 shadow-lg hover:shadow-xl">
              <span class="text-lg">Shop Now - $39.99</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" />
              </svg>
            </button>
            <button class="border-2 border-gray-300 dark:border-gray-700 hover:border-primary-600 dark:hover:border-primary-400 px-6 py-4 rounded-lg font-medium flex items-center justify-center transition duration-300 text-gray-700 dark:text-white hover:bg-white dark:hover:bg-gray-800">
              <span class="text-lg">Watch Demo</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2 text-primary-600 dark:text-primary-400" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd" />
              </svg>
            </button>
          </div>
          <div class="flex items-center space-x-4">
            <div class="flex -space-x-2">
              <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
              <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
              <img src="https://randomuser.me/api/portraits/women/24.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
            </div>
            <div class="text-sm text-gray-600 dark:text-gray-400">
              <span class="font-medium text-gray-900 dark:text-white">1,200+</span> happy customers
            </div>
            <div class="flex items-center">
              <div class="flex text-yellow-400">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                </svg>
              </div>
              <span class="ml-2 text-sm font-medium text-gray-600 dark:text-gray-400">4.9/5 rating</span>
            </div>
          </div>
        </div>
        <div class="md:w-1/2 relative hero-image-container">
          <div class="relative transform transition-all duration-700 hover:scale-[1.02] hover:rotate-1">
            <div class="absolute -top-4 -left-4 w-24 h-24 bg-yellow-400 rounded-full opacity-20 blur-xl animate-pulse-slow"></div>
            <div class="absolute -bottom-6 -right-6 w-32 h-32 bg-primary-600 dark:bg-primary-500 rounded-full opacity-20 blur-xl animate-pulse-slow animation-delay-1000"></div>
            <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-full h-full bg-gradient-to-br from-primary-500 to-blue-500 opacity-20 rounded-xl blur-3xl filter animate-pulse-slow animation-delay-2000"></div>
            <img
              src="/src/assets/product-images/hero-section-slide-1.jpg"
              alt="Under Sink Organizer Product"
              class="rounded-xl shadow-2xl w-full object-cover relative z-10 hero-image"
            />
          </div>
          <div class="absolute -bottom-6 -right-6 bg-white dark:bg-gray-800 rounded-lg shadow-lg p-4 flex items-center max-w-xs">
            <div class="bg-green-500 p-2 rounded-lg mr-3">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
            </div>
            <div>
              <p class="text-sm font-semibold text-gray-800 dark:text-white">Free Shipping</p>
              <p class="text-xs text-gray-500 dark:text-gray-400">On orders over $25</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',
  data() {
    return {
      mobileMenuOpen: false,
      isDarkMode: false
    }
  },
  mounted() {
    // Check system or localStorage preference for dark mode
    this.isDarkMode = document.documentElement.classList.contains('dark');
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen;
    },
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
      if (this.isDarkMode) {
        document.documentElement.classList.add('dark');
        localStorage.theme = 'dark';
      } else {
        document.documentElement.classList.remove('dark');
        localStorage.theme = 'light';
      }
    }
  },
}
</script>

<style scoped>
/* Add styles for mobile menu animation */
.mobile-menu-enter-active,
.mobile-menu-leave-active {
  transition: all 0.3s ease;
}

.mobile-menu-enter-from,
.mobile-menu-leave-to {
  opacity: 0;
  transform: translateY(-20px);
}

/* Header animations */
.header-animated {
  animation: slideInDown 0.5s forwards;
}

/* Logo animations */
.logo-animated {
  animation: fadeIn 0.8s forwards;
}

.logo-icon {
  animation: rotateIn 1s forwards;
  transform-origin: center;
}

/* Navigation links hover effect */
.nav-link::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 50%;
  width: 0;
  height: 2px;
  background: currentColor;
  transition: all 0.3s ease;
  transform: translateX(-50%);
}

.nav-link:hover::after {
  width: 100%;
}

.nav-links a {
  animation: fadeInStaggered 0.5s forwards;
  opacity: 0;
}

.nav-links a:nth-child(1) { animation-delay: 0.1s; }
.nav-links a:nth-child(2) { animation-delay: 0.2s; }
.nav-links a:nth-child(3) { animation-delay: 0.3s; }
.nav-links a:nth-child(4) { animation-delay: 0.4s; }
.nav-links a:nth-child(5) { animation-delay: 0.5s; }

/* Button animations */
.btn-animated::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: all 0.5s ease;
}

.btn-animated:hover::after {
  left: 100%;
}

/* Hero content animations */
.hero-content > * {
  opacity: 0;
  animation: fadeInUp 0.8s forwards;
}

.badge-animated {
  animation-delay: 0.2s;
}

.hero-title {
  animation-delay: 0.4s;
}

.hero-description {
  animation-delay: 0.6s;
}

.features-icons {
  animation-delay: 0.8s;
}

.feature-item {
  opacity: 0;
  animation: fadeInRight 0.5s forwards;
}

.feature-item:nth-child(1) { animation-delay: 0.9s; }
.feature-item:nth-child(2) { animation-delay: 1s; }
.feature-item:nth-child(3) { animation-delay: 1.1s; }

.hero-cta {
  animation-delay: 1.2s;
}

.hero-image-container {
  animation: fadeInRight 1s 0.7s forwards;
  opacity: 0;
}

.hero-image {
  animation: zoomIn 1.5s 1.2s forwards;
  transform: scale(0.95);
  opacity: 0.8;
}

/* Gradient text */
.gradient-text {
  background: linear-gradient(90deg, #3B82F6, #10B981);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  position: relative;
  display: inline-block;
}

/* Blob animation */
@keyframes blob {
  0% { transform: translate(0, 0) scale(1); }
  33% { transform: translate(20px, -20px) scale(1.1); }
  66% { transform: translate(-20px, 20px) scale(0.9); }
  100% { transform: translate(0, 0) scale(1); }
}

.animate-blob {
  animation: blob 10s infinite alternate;
}

.animation-delay-2000 {
  animation-delay: 2s;
}

.animation-delay-4000 {
  animation-delay: 4s;
}

.animation-delay-1000 {
  animation-delay: 1s;
}

/* Custom animations keyframes */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInRight {
  from { opacity: 0; transform: translateX(-20px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes fadeInStaggered {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes rotateIn {
  from { transform: rotate(-20deg); opacity: 0; }
  to { transform: rotate(0); opacity: 1; }
}

@keyframes zoomIn {
  from { transform: scale(0.95); opacity: 0.8; }
  to { transform: scale(1); opacity: 1; }
}

@keyframes slideInDown {
  from { transform: translateY(-20px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

@keyframes bounce-x {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(3px); }
}

.animate-bounce-x {
  animation: bounce-x 1s infinite;
}

/* Responsive adjustments for animations */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
  }
}

.btn-primary {
  @apply inline-flex items-center justify-center px-6 py-3 bg-primary-600 dark:bg-primary-700 text-white font-medium rounded-lg hover:bg-primary-700 dark:hover:bg-primary-600 transition duration-300 ease-in-out;
}

.btn-secondary {
  @apply inline-flex items-center justify-center px-6 py-3 bg-white dark:bg-gray-800 text-primary-600 dark:text-primary-400 border border-primary-600 dark:border-primary-400 font-medium rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700 transition duration-300 ease-in-out;
}
</style>
