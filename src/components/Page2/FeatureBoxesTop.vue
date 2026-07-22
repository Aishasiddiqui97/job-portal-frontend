<template>
  <!-- EXACT: Feature Boxes from Page 2 Top -->
  <section class="bg-gray-50 px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <!-- 3-Column Feature Boxes -->
      <div class="grid grid-cols-3 gap-4">
        <div v-for="feature in features" :key="feature.id"
             class="bg-white p-4 rounded border border-gray-200">
          <!-- Icon -->
          <div class="w-10 h-10 bg-blue-100 rounded mb-3 flex items-center justify-center">
            <span class="text-xl">{{ feature.icon }}</span>
          </div>
          
          <!-- Content -->
          <h3 class="font-bold text-sm text-gray-900 mb-1">{{ feature.title }}</h3>
          <p class="text-xs text-gray-600 leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  { id: 1, icon: '🎯', title: 'Find the Right Job', description: 'Search through thousands of opportunities' },
  { id: 2, icon: '📄', title: 'Easy Application', description: 'Apply with just one click' },
  { id: 3, icon: '🤝', title: 'Get Hired Fast', description: 'Connect with top employers' }
]
</script>
