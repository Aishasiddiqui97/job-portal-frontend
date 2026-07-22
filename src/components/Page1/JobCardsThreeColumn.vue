<template>
  <!-- EXACT: 3-Column Job Cards from Page 1 -->
  <section class="bg-gray-50 px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-lg font-bold text-gray-900">Recent Jobs</h2>
        <a href="#" class="text-blue-600 text-sm">View All →</a>
      </div>
      
      <!-- 3-Column Grid -->
      <div class="grid grid-cols-3 gap-4">
        <div v-for="job in jobs" :key="job.id" 
             class="bg-white border border-gray-200 rounded p-3 hover:shadow-md transition">
          <!-- Image -->
          <div class="aspect-video bg-gray-200 rounded mb-2 overflow-hidden">
            <img :src="job.image" 
                 class="w-full h-full object-cover" :alt="job.title" />
          </div>
          
          <!-- Content -->
          <h3 class="font-semibold text-sm text-gray-900 mb-1">{{ job.title }}</h3>
          <p class="text-xs text-gray-600 mb-2">{{ job.company }}</p>
          <div class="flex items-center justify-between text-xs">
            <span class="text-gray-500">{{ job.location }}</span>
            <span class="text-blue-600 font-semibold">{{ job.salary }}</span>
          </div>
          <p class="text-xs text-gray-400 mt-1">{{ job.posted }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  { 
    id: 1, 
    title: 'UI/UX Designer', 
    company: 'TechCorp', 
    location: 'Remote', 
    salary: '$80k - $100k', 
    posted: '2 days ago',
    image: 'https://images.unsplash.com/photo-1559028012-481c04fa702d?w=400&h=250&fit=crop'
  },
  { 
    id: 2, 
    title: 'Frontend Developer', 
    company: 'StartupXYZ', 
    location: 'San Francisco', 
    salary: '$100k - $130k', 
    posted: '1 day ago',
    image: 'https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=400&h=250&fit=crop'
  },
  { 
    id: 3, 
    title: 'Product Manager', 
    company: 'BigCo', 
    location: 'New York', 
    salary: '$120k - $150k', 
    posted: '3 days ago',
    image: 'https://images.unsplash.com/photo-1542744173-8e7e53415bb0?w=400&h=250&fit=crop'
  }
]
</script>
