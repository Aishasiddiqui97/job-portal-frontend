<template>
  <!-- EXACT: Blog/Articles List from Page 1 -->
  <section class="bg-white px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-lg font-bold text-gray-900 mb-4">Career Tips & Resources</h2>
      
      <!-- Vertical List -->
      <div class="space-y-3">
        <div v-for="article in articles" :key="article.id"
             class="flex gap-3 p-3 border border-gray-200 rounded hover:bg-gray-50 transition">
          <!-- Icon/Image -->
          <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-purple-100 rounded flex items-center justify-center flex-shrink-0">
            <span class="text-2xl">{{ article.icon }}</span>
          </div>
          
          <!-- Content -->
          <div class="flex-1">
            <h3 class="font-semibold text-sm text-gray-900 mb-1">{{ article.title }}</h3>
            <p class="text-xs text-gray-600 mb-1">{{ article.excerpt }}</p>
            <div class="flex items-center justify-between">
              <span class="text-xs text-gray-400">{{ article.date }}</span>
              <a href="#" class="text-xs text-blue-600 hover:underline">Read →</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const articles = [
  { id: 1, icon: '📝', title: 'How to Write a Perfect Resume', excerpt: 'Tips for creating standout resumes...', date: 'May 15' },
  { id: 2, icon: '💼', title: 'Interview Preparation Guide', excerpt: 'Master your next job interview...', date: 'May 12' },
  { id: 3, icon: '🚀', title: 'Career Growth in 2024', excerpt: 'Advance your career with these tips...', date: 'May 10' }
]
</script>
