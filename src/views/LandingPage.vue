<template>
  <div class="landing-page">
    <!-- Hero Section - No animation for first section -->
    <section class="bg-gradient-to-b from-blue-50 to-white dark:from-gray-900 dark:to-gray-800">
      <HeroSection /> 
    </section>

    <!-- Features Section -->
    <section 
      ref="featuresSection"
      class="relative ml-10 w-full py-16 mb-4 bg-white dark:bg-gray-900 section-animate" 
      :class="{'section-visible': visibleSections.features}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <FeaturesSection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.features}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.features && !visibleSections.painPoints}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- Pain Points Section -->
    <section 
      ref="painPointsSection"
      class="relative py-16 mb-4 bg-gray-50 dark:bg-gray-800 section-animate" 
      :class="{'section-visible': visibleSections.painPoints}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <PainPointsSection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.painPoints}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.painPoints && !visibleSections.specifications}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- Specifications Section -->
    <section 
      ref="specificationsSection"
      class="relative ml-10 w-full py-16 bg-white dark:bg-gray-900 section-animate" 
      :class="{'section-visible': visibleSections.specifications}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <SpecificationsSection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.specifications}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.specifications && !visibleSections.company}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- Company Information -->
    <section 
      ref="companySection"
      class="relative py-16 mb-4 bg-white dark:bg-gray-900 section-animate" 
      :class="{'section-visible': visibleSections.company}"
    >
      <div class="">
        <CompanySection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.company}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.company && !visibleSections.testimonials}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- Customer Examples -->
    <section 
      ref="testimonialsSection"
      class="relative py-16 mb-4 bg-white dark:bg-gray-900 section-animate" 
      :class="{'section-visible': visibleSections.testimonials}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <TestimonialsSection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.testimonials}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.testimonials && !visibleSections.faq}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section 
      ref="faqSection"
      class="relative py-16 mb-4 bg-gray-50 dark:bg-gray-800 section-animate" 
      :class="{'section-visible': visibleSections.faq}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <FaqSection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.faq}"></div>
      <!-- Section transition indicator -->
      <div class="section-transition" :class="{'active': visibleSections.faq && !visibleSections.cta}">
        <div class="scroll-indicator">
          <div class="chevron"></div>
          <div class="chevron"></div>
          <div class="chevron"></div>
          <span class="scroll-text"></span>
        </div>
      </div>
    </section>

    <!-- Call-to-Action (CTA) -->
    <section 
      ref="ctaSection"
      class="relative ml-10 w-full bg-primary-600 dark:bg-primary-700 section-animate" 
      :class="{'section-visible': visibleSections.cta}"
    >
      <div class="container mx-auto px-4 md:px-6">
        <CTASection />
      </div>
      <!-- Section loader indicator -->
      <div class="section-loader" :class="{'loaded': visibleSections.cta}"></div>
    </section>

    <!-- Footer -->
    <footer class="py-8 bg-gray-900 text-white">
      <FooterSection />
    </footer>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useIntersectionObserver } from '@vueuse/core'

import HeroSection from '../components/HeroSection.vue'
import FeaturesSection from '../components/FeaturesSection.vue'
import PainPointsSection from '../components/PainPointsSection.vue'
import SpecificationsSection from '../components/SpecificationsSection.vue'
import CompanySection from '../components/CompanySection.vue'
import TestimonialsSection from '../components/TestimonialsSection.vue'
import FaqSection from '../components/FaqSection.vue'
import CTASection from '../components/CTASection.vue'
import FooterSection from '../components/FooterSection.vue'

export default {
  name: 'LandingPage',
  components: {
    HeroSection,
    FeaturesSection,
    PainPointsSection,
    SpecificationsSection,
    CompanySection,
    TestimonialsSection,
    FaqSection,
    CTASection,
    FooterSection
  },
  data() {
    return {
      // Track which sections are visible
      visibleSections: {
        features: false,
        painPoints: false,
        specifications: false,
        company: false,
        testimonials: false,
        faq: false,
        cta: false
      },
      observers: []
    }
  },
  mounted() {
    // Setup intersection observers for all sections and elements
    this.$nextTick(() => {
      this.setupSectionObservers()
      this.setupElementAnimations()
    })
  },
  beforeUnmount() {
    // Cleanup any observers created with native IntersectionObserver
    this.observers.forEach(observer => observer.disconnect())
    // VueUse observers are cleaned up automatically
  },

  methods: {
    setupCrossBrowserCompatibility() {
      // Detect browser and add appropriate class to body for CSS targeting
      const isIE = /*@cc_on!@*/false || !!document.documentMode;
      const isEdge = !isIE && !!window.StyleMedia;
      const isChrome = !!window.chrome && (!!window.chrome.webstore || !!window.chrome.runtime);
      const isFirefox = typeof InstallTrigger !== 'undefined';
      const isSafari = /constructor/i.test(window.HTMLElement) || 
          (function (p) { return p.toString() === "[object SafariRemoteNotification]"; })(!window['safari'] || 
          (typeof safari !== 'undefined' && safari.pushNotification));
      
      // Add browser classes to body
      if (isIE) document.body.classList.add('is-ie');
      if (isEdge) document.body.classList.add('is-edge');
      if (isChrome) document.body.classList.add('is-chrome');
      if (isFirefox) document.body.classList.add('is-firefox');
      if (isSafari) document.body.classList.add('is-safari');
      
      // Add fallbacks for CSS variables if not supported
      if (!window.CSS || !window.CSS.supports || !window.CSS.supports('--fake-var', 0)) {
        // Add polyfill for CSS variables
        const style = document.createElement('style');
        style.innerHTML = `
          .chevron:before, .chevron:after { background: #4F46E5; }
          .dark .chevron:before, .dark .chevron:after { background: #818CF8; }
          .scroll-text { color: #4F46E5; }
          .dark .scroll-text { color: #818CF8; }
        `;
        document.head.appendChild(style);
      }
    },
    setupSectionObservers() {
      // Create an observer for each section using VueUse
      const sections = [
        { ref: 'featuresSection', key: 'features' },
        { ref: 'painPointsSection', key: 'painPoints' },
        { ref: 'specificationsSection', key: 'specifications' },
        { ref: 'companySection', key: 'company' },
        { ref: 'testimonialsSection', key: 'testimonials' },
        { ref: 'faqSection', key: 'faq' },
        { ref: 'ctaSection', key: 'cta' }
      ]
      
      // Setup each section with useIntersectionObserver
      sections.forEach(section => {
        if (this.$refs[section.ref]) {
          const stop = useIntersectionObserver(
            this.$refs[section.ref],
            (entries) => {
              const isIntersecting = entries[0]?.isIntersecting
              if (isIntersecting) {
                this.visibleSections[section.key] = true
                // Once triggered, can stop observing
                stop()
              }
            },
            { threshold: 0.05, rootMargin: '-10px 0px -10px 0px' }
          )
        }
      })
    },
    setupElementAnimations() {
      // Get all elements with 'reveal' class
      const revealElements = document.querySelectorAll('.reveal')
      const staggerElements = document.querySelectorAll('.stagger-reveal')
      
      // Options for the observer
      const observerOptions = {
        threshold: 0.05,
        rootMargin: '0px 0px -10% 0px'
      }
      
      // Create observer for individual reveal elements
      if (revealElements.length > 0) {
        const revealObserver = new IntersectionObserver((entries) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              entry.target.classList.add('visible')
              // Stop observing after animation triggered
              revealObserver.unobserve(entry.target)
            }
          })
        }, observerOptions)
        
        revealElements.forEach(el => {
          revealObserver.observe(el)
        })
        
        this.observers.push(revealObserver)
      }
      
      // Create observer for staggered reveal elements
      if (staggerElements.length > 0) {
        const staggerObserver = new IntersectionObserver((entries) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              entry.target.classList.add('visible')
              // Stop observing after animation triggered
              staggerObserver.unobserve(entry.target)
            }
          })
        }, observerOptions)
        
        staggerElements.forEach(el => {
          staggerObserver.observe(el)
        })
        
        this.observers.push(staggerObserver)
      }
    }
  }
}
</script>

<style scoped>
/* Section animation styles with varied entrance animations */
.section-animate {
  opacity: 0;
  transition: opacity 1.2s cubic-bezier(0.16, 1, 0.3, 1), transform 1.2s cubic-bezier(0.16, 1, 0.3, 1);
}

/* Create different entrance animations for alternating sections */
.section-animate:nth-child(odd) {
  transform: translateY(40px);
}

.section-animate:nth-child(even) {
  transform: translateX(-40px);
}

.section-visible {
  opacity: 1;
  transform: translateY(0) translateX(0);
}

/* Fancy entrance effects */
.section-animate.section-visible {
  animation-duration: 0.5s;
  animation-fill-mode: both;
  animation-timing-function: cubic-bezier(0.5, 0, 0.1, 1);
}

/* Add subtle parallax effect to sections */
.landing-page {
  perspective: 1000px;
}

/* Enhanced fade between sections with gradient effect */
section {
  position: relative;
  transition: all 0.5s ease;
  overflow: hidden;
}

/* section:hover {
  transform: translateZ(5px); 
} */

section::before {
  content: '';
  position: absolute;
  top: -5px;
  left: 0;
  width: 100%;
  height: 5px;
  background: linear-gradient(to top, transparent, rgba(0, 0, 0, 0.03));
  pointer-events: none;
}

section::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 15px;
  background: linear-gradient(to bottom, transparent, rgba(0, 0, 0, 0.04));
  pointer-events: none;
  opacity: 0.7;
  transition: opacity 0.3s ease;
}

section:hover::after {
  opacity: 1;
}

section:last-of-type::after {
  display: none;
}

/* Scroll-based parallax decorations */
.landing-page::before {
  content: '';
  position: fixed;
  top: 0;
  right: 0;
  width: 30vw;
  height: 30vw;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.05) 0%, rgba(59, 130, 246, 0) 70%);
  pointer-events: none;
  z-index: -1;
  transform-origin: center;
  animation: float-slow 15s infinite alternate ease-in-out;
}

.landing-page::after {
  content: '';
  position: fixed;
  bottom: 10vh;
  left: 5vw;
  width: 20vw;
  height: 20vw;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(16, 185, 129, 0.05) 0%, rgba(16, 185, 129, 0) 70%);
  pointer-events: none;
  z-index: -1;
  animation: float-slow 10s infinite alternate-reverse ease-in-out;
}

@keyframes float-slow {
  0% {
    transform: translateY(0) scale(1);
  }
  100% {
    transform: translateY(30px) scale(1.05);
  }
}
/* Section loader indicator */
.section-loader {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, rgba(79, 70, 229, 0.1) 0%, rgba(79, 70, 229, 0.2) 50%, rgba(79, 70, 229, 0.1) 100%);
  transform: scaleX(0);
  transform-origin: left;
  opacity: 0.7;
  transition: transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  z-index: 20;
}

.dark .section-loader {
  background: linear-gradient(90deg, rgba(129, 140, 248, 0.1) 0%, rgba(129, 140, 248, 0.2) 50%, rgba(129, 140, 248, 0.1) 100%);
}

.section-loader:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100px;
  background: linear-gradient(90deg, transparent, rgba(79, 70, 229, 0.8), transparent);
  animation: loading 1s infinite;
}

.dark .section-loader:before {
  background: linear-gradient(90deg, transparent, rgba(129, 140, 248, 0.8), transparent);
}

.section-loader.loaded {
  transform: scaleX(1);
}

@keyframes loading {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

/* Section transition indicators */
.section-transition {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0;
  transition: opacity 0.5s ease;
  z-index: 10;
}

.section-transition.active {
  opacity: 1;
}

.scroll-indicator {
  display: flex;
  flex-direction: column;
  align-items: center;
  cursor: pointer;
}

.chevron {
  width: 20px;
  height: 8px;
  opacity: 0;
  transform: scale(0.3);
  animation: move-chevron 3s ease-out infinite;
}

.chevron:first-child {
  animation: move-chevron 2s ease-out 0.5s infinite;
}

.chevron:nth-child(2) {
  animation: move-chevron 2s ease-out 1s infinite;
}

.chevron:before,
.chevron:after {
  content: '';
  position: absolute;
  top: 0;
  height: 100%;
  width: 50%;
  background: var(--color-primary-600, #4F46E5);
}

.dark .chevron:before,
.dark .chevron:after {
  background: var(--color-primary-400, #818CF8);
}

.chevron:before {
  left: 0;
  transform: skewY(30deg);
}

.chevron:after {
  right: 0;
  width: 50%;
  transform: skewY(-30deg);
}

.scroll-text {
  font-size: 12px;
  margin-top: 5px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: var(--color-primary-600, #4F46E5);
  animation: fade-in-out 3s ease-in-out infinite;
}

.dark .scroll-text {
  color: var(--color-primary-400, #818CF8);
}

@keyframes move-chevron {
  25% {
    opacity: 1;
    transform: translateY(15px) scale(1);
  }
  33% { opacity: 1; transform: translateY(15px) scale(0.9); }
  66% { opacity: 0.6; transform: translateY(25px) scale(0.7); }
  100% { opacity: 0; transform: translateY(30px) scale(0.5); }
}

@keyframes fade-in-out {
  0%, 100% { opacity: 0.5; }
  50% { opacity: 1; }
}

/* Cross-browser compatibility CSS */
:root {
  --color-primary-600: #4F46E5;
  --color-primary-400: #818CF8;
}

/* Ensure animations work in older browsers */
@supports not (animation-name: move-chevron) {
  .chevron, .scroll-text {
    opacity: 0.8;
    transform: none;
  }
}
</style>
