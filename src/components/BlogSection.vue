<template>
  <!-- Blog/Articles Section (From Figma Page 1) -->
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center mb-12">
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-2">
            Career Tips & Insights
          </h2>
          <p class="text-gray-600">
            Latest articles to help you succeed
          </p>
        </div>
        <button class="text-blue-600 font-medium hover:text-blue-700 flex items-center gap-2">
          View All Articles
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <article v-for="article in articles" :key="article.id"
                 class="bg-white border border-gray-200 rounded-2xl overflow-hidden hover:shadow-xl transition-all group cursor-pointer">
          <!-- Article Image -->
          <div class="aspect-video bg-gradient-to-br from-blue-100 to-purple-100 flex items-center justify-center text-6xl group-hover:scale-105 transition-transform">
            {{ article.emoji }}
          </div>
          
          <!-- Article Content -->
          <div class="p-6">
            <div class="flex items-center gap-3 mb-3">
              <span class="px-3 py-1 bg-blue-100 text-blue-700 text-xs font-medium rounded-full">
                {{ article.category }}
              </span>
              <span class="text-xs text-gray-500">{{ article.date }}</span>
            </div>
            
            <h3 class="text-xl font-semibold text-gray-900 mb-2 group-hover:text-blue-600 line-clamp-2">
              {{ article.title }}
            </h3>
            
            <p class="text-gray-600 text-sm line-clamp-3 mb-4">
              {{ article.excerpt }}
            </p>
            
            <div class="flex items-center justify-between pt-4 border-t border-gray-100">
              <div class="flex items-center gap-2">
                <div class="w-8 h-8 bg-gradient-to-br from-blue-500 to-purple-500 rounded-full"></div>
                <span class="text-sm font-medium text-gray-700">{{ article.author }}</span>
              </div>
              <button class="text-blue-600 text-sm font-medium hover:text-blue-700">
                Read More →
              </button>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const articles = [
  {
    id: 1,
    emoji: '📝',
    category: 'Career Tips',
    date: 'May 15, 2024',
    title: 'How to Write a Perfect Resume in 2024',
    excerpt: 'Learn the essential tips and tricks to create a resume that stands out and gets you noticed by recruiters.',
    author: 'Sarah Johnson'
  },
  {
    id: 2,
    emoji: '💼',
    category: 'Interview',
    date: 'May 12, 2024',
    title: '10 Common Interview Questions and How to Answer',
    excerpt: 'Master the most frequently asked interview questions and increase your chances of landing your dream job.',
    author: 'Michael Chen'
  },
  {
    id: 3,
    emoji: '🚀',
    category: 'Career Growth',
    date: 'May 10, 2024',
    title: 'Career Change: When and How to Make the Switch',
    excerpt: 'Thinking about changing careers? Here\'s everything you need to know to make a smooth transition.',
    author: 'Emily Rodriguez'
  }
]
</script>
