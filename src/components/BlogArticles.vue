<template>
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex justify-between items-center mb-12">
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-2">
            Career Tips & Articles
          </h2>
          <p class="text-gray-600">
            Get expert advice for your job search
          </p>
        </div>
        <button class="text-primary-600 font-medium hover:text-primary-700 flex items-center gap-2">
          View All
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <article 
          v-for="article in articles" 
          :key="article.id"
          class="bg-white rounded-xl overflow-hidden hover:shadow-xl transition-shadow border border-gray-200 cursor-pointer group"
        >
          <div class="aspect-video bg-gray-200 overflow-hidden">
            <img 
              :src="article.image" 
              :alt="article.title"
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
            />
          </div>
          
          <div class="p-6">
            <div class="flex items-center gap-2 text-sm text-gray-500 mb-3">
              <span>{{ article.category }}</span>
              <span>•</span>
              <span>{{ article.date }}</span>
            </div>
            
            <h3 class="text-xl font-semibold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors">
              {{ article.title }}
            </h3>
            
            <p class="text-gray-600 mb-4 line-clamp-2">
              {{ article.excerpt }}
            </p>
            
            <button class="text-primary-600 font-medium hover:text-primary-700 flex items-center gap-2">
              Read More
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
              </svg>
            </button>
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
    title: 'How to Write a Winning Resume in 2026',
    excerpt: 'Learn the latest tips and tricks to create a resume that stands out from the crowd and gets you noticed by recruiters.',
    category: 'Resume Tips',
    date: 'Jan 15, 2026',
    image: 'https://via.placeholder.com/400x250'
  },
  {
    id: 2,
    title: 'Top 10 Interview Questions and How to Answer Them',
    excerpt: 'Prepare for your next interview with these common questions and expert-approved answers that will impress any hiring manager.',
    category: 'Interview Tips',
    date: 'Jan 12, 2026',
    image: 'https://via.placeholder.com/400x250'
  },
  {
    id: 3,
    title: 'Remote Work: Best Practices for Success',
    excerpt: 'Discover the essential strategies and tools you need to thrive in a remote work environment and maintain work-life balance.',
    category: 'Career Advice',
    date: 'Jan 10, 2026',
    image: 'https://via.placeholder.com/400x250'
  }
]
</script>
