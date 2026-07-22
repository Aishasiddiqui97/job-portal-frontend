<template>
  <!-- Popular Categories with Tags (From Figma Page 2) -->
  <section class="py-12 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center mb-8">
        <div>
          <h2 class="text-2xl font-bold text-gray-900 mb-2">
            Popular Categories
          </h2>
          <p class="text-gray-600">
            Browse jobs by category
          </p>
        </div>
        <button class="text-blue-600 font-medium hover:text-blue-700 flex items-center gap-2">
          View All
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <!-- Category Tags -->
      <div class="flex flex-wrap gap-3">
        <button v-for="(category, index) in categories" :key="index"
                :class="[
                  'px-5 py-2.5 rounded-full text-sm font-medium transition-all',
                  category.active 
                    ? 'bg-blue-600 text-white shadow-lg shadow-blue-200' 
                    : 'bg-white text-gray-700 border border-gray-300 hover:border-blue-500 hover:text-blue-600'
                ]">
          {{ category.name }}
          <span v-if="category.count" class="ml-2 text-xs opacity-75">
            ({{ category.count }})
          </span>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const categories = [
  { name: 'All', active: true, count: 1250 },
  { name: 'Design', active: false, count: 305 },
  { name: 'Development', active: false, count: 450 },
  { name: 'Marketing', active: false, count: 180 },
  { name: 'Finance', active: false, count: 95 },
  { name: 'Customer Service', active: false, count: 125 },
  { name: 'Healthcare', active: false, count: 85 },
  { name: 'Education', active: false, count: 65 }
]
</script>
