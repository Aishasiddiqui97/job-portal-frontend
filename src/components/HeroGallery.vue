<template>
  <!-- Hero Section with Image Gallery (From Figma Page 1) -->
  <section class="bg-gradient-to-br from-blue-50 via-white to-purple-50 py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
        <!-- Left: Image Gallery Grid -->
        <div class="grid grid-cols-3 gap-3">
          <div v-for="(img, index) in galleryImages" :key="index" 
               class="aspect-square bg-gradient-to-br from-blue-100 to-purple-100 rounded-xl overflow-hidden hover:scale-105 transition-transform">
            <div class="w-full h-full flex items-center justify-center text-4xl">
              {{ img.emoji }}
            </div>
          </div>
        </div>

        <!-- Right: Hero Content -->
        <div class="space-y-6">
          <div class="inline-block px-4 py-2 bg-blue-100 text-blue-700 rounded-full text-sm font-medium">
            🎯 Over 10,000+ Jobs Available
          </div>
          
          <h1 class="text-4xl lg:text-5xl font-bold text-gray-900 leading-tight">
            Find Your Dream Job
            <span class="block text-blue-600">With Us Today</span>
          </h1>
          
          <p class="text-lg text-gray-600">
            Search and connect with the right candidates faster. Browse through thousands of job opportunities from top companies.
          </p>
          
          <div class="flex flex-wrap gap-4">
            <button class="btn-primary px-8 py-3 text-lg">
              Get Started
            </button>
            <button class="btn-secondary px-8 py-3 text-lg">
              Learn More
            </button>
          </div>
          
          <!-- Stats -->
          <div class="grid grid-cols-3 gap-6 pt-6 border-t border-gray-200">
            <div>
              <div class="text-3xl font-bold text-gray-900">10K+</div>
              <div class="text-sm text-gray-600">Active Jobs</div>
            </div>
            <div>
              <div class="text-3xl font-bold text-gray-900">5K+</div>
              <div class="text-sm text-gray-600">Companies</div>
            </div>
            <div>
              <div class="text-3xl font-bold text-gray-900">8K+</div>
              <div class="text-sm text-gray-600">Candidates</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const galleryImages = [
  { emoji: '💼' }, { emoji: '🎯' }, { emoji: '🚀' },
  { emoji: '💻' }, { emoji: '📱' }, { emoji: '🎨' },
  { emoji: '📊' }, { emoji: '🏆' }, { emoji: '⚡' }
]
</script>
