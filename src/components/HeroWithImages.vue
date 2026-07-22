<template>
  <!-- Hero Section - Exact from Figma Screenshot Page 1 -->
  <section class="bg-white py-8">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Image Gallery Grid - Top Section from Figma -->
      <div class="grid grid-cols-2 md:grid-cols-5 gap-3 mb-8">
        <div v-for="(img, index) in images" :key="index"
             class="aspect-video bg-gradient-to-br from-gray-100 to-gray-200 rounded-lg overflow-hidden relative group">
          <img v-if="img.url" :src="img.url" class="w-full h-full object-cover" :alt="img.alt" />
          <div v-else class="w-full h-full flex items-center justify-center bg-gray-200">
            <span class="text-3xl">{{ img.emoji }}</span>
          </div>
          <!-- Overlay on last large image -->
          <div v-if="index === 4" class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent flex items-end p-4">
            <div class="text-white">
              <h3 class="font-bold text-lg mb-1">Find Your Dream Job</h3>
              <p class="text-sm">Start your career journey today</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const images = [
  { emoji: '💼', alt: 'Business' },
  { emoji: '🎯', alt: 'Target' },
  { emoji: '📊', alt: 'Analytics' },
  { emoji: '💻', alt: 'Tech' },
  { emoji: '🚀', alt: 'Growth' }, // Large featured image
  { emoji: '📱', alt: 'Mobile' },
  { emoji: '🎨', alt: 'Design' },
  { emoji: '⚡', alt: 'Fast' },
  { emoji: '🏆', alt: 'Success' },
  { emoji: '🌟', alt: 'Featured' }
]
</script>
