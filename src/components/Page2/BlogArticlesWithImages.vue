<template>
  <!-- EXACT: Blog Articles with Large Images from Page 2 -->
  <section class="bg-white px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-lg font-bold text-gray-900 mb-4">Latest Articles</h2>
      
      <!-- Article Grid -->
      <div class="space-y-4">
        <div v-for="article in articles" :key="article.id"
             class="flex gap-4 border border-gray-200 rounded p-3 hover:bg-gray-50 transition">
          <!-- Large Image -->
          <div class="w-32 h-20 bg-gray-200 rounded flex-shrink-0 overflow-hidden">
            <img :src="article.image" 
                 class="w-full h-full object-cover" :alt="article.title" />
          </div>
          
          <!-- Content -->
          <div class="flex-1">
            <h3 class="font-semibold text-sm text-gray-900 mb-1">{{ article.title }}</h3>
            <p class="text-xs text-gray-600 mb-2">{{ article.excerpt }}</p>
            <div class="flex items-center justify-between">
              <span class="text-xs text-gray-400">{{ article.date }}</span>
              <a href="#" class="text-xs text-blue-600">Read more →</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const articles = [
  { 
    id: 1, 
    title: 'Top Career Tips for 2024', 
    excerpt: 'Essential advice for job seekers to succeed in the modern workplace...', 
    date: 'May 15, 2024',
    image: 'https://images.unsplash.com/photo-1521737711867-e3b97375f902?w=200&h=120&fit=crop'
  },
  { 
    id: 2, 
    title: 'Interview Success Guide', 
    excerpt: 'Learn how to ace your interviews with these proven strategies...', 
    date: 'May 12, 2024',
    image: 'https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?w=200&h=120&fit=crop'
  }
]
</script>
