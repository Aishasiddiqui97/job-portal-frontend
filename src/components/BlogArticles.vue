<template>
  <!-- Blog/Articles Section - From Figma Page 1 Bottom -->
  <section class="bg-gray-50 py-10">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Header -->
      <div class="flex justify-between items-center mb-6">
        <div>
          <h2 class="text-2xl font-bold text-gray-900 mb-2">Career Tips & Resources</h2>
          <p class="text-gray-600">Latest articles to boost your career</p>
        </div>
        <a href="#" class="text-blue-600 text-sm font-medium hover:text-blue-700">View all →</a>
      </div>

      <!-- Articles List -->
      <div class="space-y-4">
        <article v-for="article in articles" :key="article.id"
                 class="bg-white border border-gray-200 rounded-lg p-4 hover:shadow-md transition-shadow flex gap-4">
          <!-- Article Image/Icon -->
          <div class="w-20 h-20 bg-gradient-to-br from-blue-100 to-purple-100 rounded flex items-center justify-center flex-shrink-0">
            <span class="text-3xl">{{ article.icon }}</span>
          </div>

          <!-- Article Content -->
          <div class="flex-1">
            <h3 class="font-semibold text-gray-900 mb-1">{{ article.title }}</h3>
            <p class="text-sm text-gray-600 mb-2">{{ article.excerpt }}</p>
            <div class="flex items-center justify-between">
              <span class="text-xs text-gray-500">{{ article.date }}</span>
              <a href="#" class="text-sm text-blue-600 hover:text-blue-700 font-medium">Read more →</a>
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
    icon: '📝',
    title: 'How to Write a Winning Resume',
    excerpt: 'Learn the essential tips to create a resume that stands out...',
    date: 'May 15, 2024'
  },
  {
    id: 2,
    icon: '💼',
    title: '10 Interview Questions You Should Prepare For',
    excerpt: 'Master these common interview questions to ace your next interview...',
    date: 'May 12, 2024'
  },
  {
    id: 3,
    icon: '🚀',
    title: 'Career Growth Tips for 2024',
    excerpt: 'Essential strategies to advance your career in the new year...',
    date: 'May 10, 2024'
  }
]
</script>
