<template>
  <!-- Category Grid with Round Icons - Exact from Figma Screenshot -->
  <section class="bg-white py-10">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Section Header -->
      <div class="mb-8">
        <h2 class="text-2xl font-bold text-gray-900 mb-2">Browse by Category</h2>
        <p class="text-gray-600">Find the job that's perfect for you</p>
      </div>

      <!-- Category Icons Grid - Circular Icons like in Figma -->
      <div class="grid grid-cols-3 md:grid-cols-6 lg:grid-cols-9 gap-6">
        <div v-for="(category, index) in categories" :key="index"
             class="flex flex-col items-center group cursor-pointer">
          <!-- Round Icon Circle -->
          <div :class="[
            'w-16 h-16 rounded-full flex items-center justify-center mb-3 transition-transform group-hover:scale-110',
            category.bgColor
          ]">
            <span class="text-2xl">{{ category.icon }}</span>
          </div>
          <!-- Category Name -->
          <span class="text-sm text-gray-700 text-center font-medium">
            {{ category.name }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const categories = [
  { icon: '💼', name: 'Business', bgColor: 'bg-blue-100' },
  { icon: '🎨', name: 'Design', bgColor: 'bg-purple-100' },
  { icon: '💻', name: 'Technology', bgColor: 'bg-green-100' },
  { icon: '📱', name: 'Mobile', bgColor: 'bg-pink-100' },
  { icon: '📊', name: 'Marketing', bgColor: 'bg-yellow-100' },
  { icon: '⚖️', name: 'Legal', bgColor: 'bg-red-100' },
  { icon: '🏥', name: 'Healthcare', bgColor: 'bg-teal-100' },
  { icon: '🎓', name: 'Education', bgColor: 'bg-indigo-100' },
  { icon: '🔧', name: 'Engineering', bgColor: 'bg-orange-100' }
]
</script>
