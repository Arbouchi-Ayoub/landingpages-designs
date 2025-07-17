<template>
  <div class="container mx-auto px-4 py-8">
    <div class="max-w-4xl mx-auto bg-white dark:bg-gray-800 rounded-2xl overflow-hidden shadow-xl">
      <div class="flex flex-col md:flex-row">
        <div class="md:w-1/2 p-8 md:p-10">
          <h2 class="text-3xl font-bold mb-4 text-gray-900 dark:text-white">Ready to Transform Your Space?</h2>
          <p class="text-gray-600 dark:text-gray-300 mb-6">
            Join thousands of satisfied customers who have revolutionized their under-sink storage. Order now and get free shipping!
          </p>
          
          <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
            <button class="btn-primary">
              Buy Now - $39.99
            </button>
            <button class="btn-secondary">
              Add to Wishlist
            </button>
          </div>
          
          <div class="mt-6 flex items-center">
            <div class="flex -space-x-2 mr-4">
              <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
              <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
              <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Customer" class="w-8 h-8 rounded-full border-2 border-white dark:border-gray-800" />
            </div>
            <p class="text-sm text-gray-500 dark:text-gray-400">
              Joined by 10,000+ happy customers this month
            </p>
          </div>
        </div>
        
        <div class="md:w-1/2 bg-primary-50 dark:bg-gray-700 p-8 md:p-10 flex flex-col justify-center">
          <div class="flex items-center mb-6">
            <div class="mr-4 text-primary-600 dark:text-primary-400">
              <svg class="w-12 h-12" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xl font-bold text-gray-900 dark:text-white">100% Satisfaction Guarantee</p>
              <p class="text-gray-600 dark:text-gray-300">30-day money back guarantee</p>
            </div>
          </div>
          
          <div class="flex items-center mb-6">
            <div class="mr-4 text-primary-600 dark:text-primary-400">
              <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xl font-bold text-gray-900 dark:text-white">Fast Delivery</p>
              <p class="text-gray-600 dark:text-gray-300">2-5 business days shipping</p>
            </div>
          </div>
          
          <div class="flex items-center">
            <div class="mr-4 text-primary-600 dark:text-primary-400">
              <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path>
              </svg>
            </div>
            <div>
              <p class="text-xl font-bold text-gray-900 dark:text-white">2-Year Warranty</p>
              <p class="text-gray-600 dark:text-gray-300">Full coverage for peace of mind</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CtaSection'
}
</script>

<style scoped>
.btn-primary {
  @apply inline-flex items-center justify-center px-6 py-3 bg-primary-600 dark:bg-primary-700 text-white font-medium rounded-lg hover:bg-primary-700 dark:hover:bg-primary-600 transition duration-300 ease-in-out;
}

.btn-secondary {
  @apply inline-flex items-center justify-center px-6 py-3 bg-white dark:bg-gray-800 text-primary-600 dark:text-primary-400 border border-primary-600 dark:border-primary-400 font-medium rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700 transition duration-300 ease-in-out;
}
</style>
