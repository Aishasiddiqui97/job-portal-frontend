<template>
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-gray-900 mb-3">
          Popular Job Categories
        </h2>
        <p class="text-gray-600">
          Explore job opportunities across different industries
        </p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <CategoryCard 
          v-for="category in categories" 
          :key="category.id"
          :icon="category.icon"
          :title="category.title"
          :count="category.count"
          :color="category.color"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import CategoryCard from './CategoryCard.vue'

const categories = [
  { id: 1, icon: '💼', title: 'Business & Finance', count: 2847, color: 'bg-blue-100' },
  { id: 2, icon: '💻', title: 'Technology & IT', count: 3245, color: 'bg-purple-100' },
  { id: 3, icon: '🎨', title: 'Design & Creative', count: 1823, color: 'bg-pink-100' },
  { id: 4, icon: '📱', title: 'Marketing & Sales', count: 2156, color: 'bg-green-100' },
  { id: 5, icon: '🏥', title: 'Healthcare', count: 1634, color: 'bg-red-100' },
  { id: 6, icon: '⚖️', title: 'Legal & Law', count: 982, color: 'bg-yellow-100' },
  { id: 7, icon: '🎓', title: 'Education', count: 1445, color: 'bg-indigo-100' },
  { id: 8, icon: '🏗️', title: 'Engineering', count: 2034, color: 'bg-orange-100' },
]
</script>
