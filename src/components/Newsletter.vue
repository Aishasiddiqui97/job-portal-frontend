<template>
  <!-- Newsletter Section (From Figma Page 2) -->
  <section class="py-20 bg-gradient-to-r from-blue-50 to-purple-50">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <div class="mb-8">
        <span class="inline-block px-4 py-2 bg-blue-100 text-blue-700 rounded-full text-sm font-medium mb-4">
          📧 Newsletter
        </span>
        <h2 class="text-4xl font-bold text-gray-900 mb-4">
          Get Weekly Job Updates
        </h2>
        <p class="text-gray-600 text-lg">
          Subscribe to our newsletter and never miss out on new job opportunities
        </p>
      </div>

      <!-- Newsletter Form -->
      <div class="bg-white rounded-2xl shadow-xl p-8 max-w-2xl mx-auto">
        <form class="flex flex-col sm:flex-row gap-4">
          <input
            type="email"
            placeholder="Enter your email address"
            class="flex-1 px-6 py-4 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none text-gray-900"
          />
          <button type="submit" class="btn-primary px-8 py-4 whitespace-nowrap">
            Subscribe Now
          </button>
        </form>
        
        <p class="text-xs text-gray-500 mt-4">
          We respect your privacy. Unsubscribe at any time.
        </p>
      </div>

      <!-- Trust Badges -->
      <div class="mt-12 flex flex-wrap justify-center items-center gap-8 text-gray-600">
        <div class="flex items-center gap-2">
          <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
          </svg>
          <span class="text-sm">10,000+ Subscribers</span>
        </div>
        <div class="flex items-center gap-2">
          <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
          </svg>
          <span class="text-sm">Weekly Updates</span>
        </div>
        <div class="flex items-center gap-2">
          <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
          </svg>
          <span class="text-sm">No Spam</span>
        </div>
      </div>
    </div>
  </section>
</template>
