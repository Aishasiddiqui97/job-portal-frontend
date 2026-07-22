<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-gray-900 mb-3">
          Browse by Category Icons
        </h2>
        <p class="text-gray-600">
          Select from our popular job categories
        </p>
      </div>

      <!-- Icon Grid (From Figma) -->
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6">
        <div 
          v-for="category in iconCategories" 
          :key="category.id"
          class="flex flex-col items-center justify-center p-6 bg-white rounded-xl hover:shadow-lg transition-all cursor-pointer group border border-gray-100"
        >
          <div 
            :class="[category.bgColor, 'w-16 h-16 rounded-full flex items-center justify-center mb-4 group-hover:scale-110 transition-transform']"
          >
            <span class="text-3xl">{{ category.icon }}</span>
          </div>
          <span class="text-sm font-medium text-gray-700 text-center">
            {{ category.name }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const iconCategories = [
  { id: 1, icon: '💼', name: 'Business', bgColor: 'bg-blue-100' },
  { id: 2, icon: '💻', name: 'Technology', bgColor: 'bg-purple-100' },
  { id: 3, icon: '🎨', name: 'Design', bgColor: 'bg-pink-100' },
  { id: 4, icon: '📱', name: 'Marketing', bgColor: 'bg-green-100' },
  { id: 5, icon: '🏥', name: 'Healthcare', bgColor: 'bg-red-100' },
  { id: 6, icon: '⚖️', name: 'Legal', bgColor: 'bg-yellow-100' },
  { id: 7, icon: '🎓', name: 'Education', bgColor: 'bg-indigo-100' },
  { id: 8, icon: '🏗️', name: 'Engineering', bgColor: 'bg-orange-100' },
  { id: 9, icon: '📊', name: 'Finance', bgColor: 'bg-cyan-100' },
  { id: 10, icon: '🎬', name: 'Media', bgColor: 'bg-purple-100' },
  { id: 11, icon: '🍔', name: 'Food', bgColor: 'bg-amber-100' },
  { id: 12, icon: '✈️', name: 'Travel', bgColor: 'bg-sky-100' },
]
</script>
