<template>
  <!-- EXACT: 4-Column Job Cards with Images from Page 2 -->
  <section class="bg-gray-50 px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-lg font-bold text-gray-900">Featured Opportunities</h2>
        <a href="#" class="text-blue-600 text-sm">See all →</a>
      </div>
      
      <!-- 4-Column Grid -->
      <div class="grid grid-cols-4 gap-3">
        <div v-for="job in jobs" :key="job.id"
             class="bg-white rounded border border-gray-200 overflow-hidden hover:shadow-md transition">
          <!-- Job Image -->
          <div class="aspect-video bg-gray-300">
            <img :src="job.image" 
                 class="w-full h-full object-cover" alt="Job" />
          </div>
          
          <!-- Content -->
          <div class="p-2">
            <h3 class="font-semibold text-xs text-gray-900 mb-1 truncate">{{ job.title }}</h3>
            <p class="text-xs text-gray-600 truncate">{{ job.company }}</p>
            <div class="flex items-center justify-between mt-2">
              <span class="text-xs text-gray-500">{{ job.location }}</span>
              <span class="text-xs text-blue-600 font-semibold">{{ job.salary }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  { 
    id: 1, 
    title: 'Senior Designer', 
    company: 'Creative Agency', 
    location: 'Remote', 
    salary: '$90k+',
    image: 'https://images.unsplash.com/photo-1586717791821-3f44a563fa4c?w=300&h=200&fit=crop'
  },
  { 
    id: 2, 
    title: 'Software Developer', 
    company: 'Tech Company', 
    location: 'San Francisco', 
    salary: '$110k+',
    image: 'https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?w=300&h=200&fit=crop'
  },
  { 
    id: 3, 
    title: 'Project Manager', 
    company: 'Enterprise Corp', 
    location: 'New York', 
    salary: '$100k+',
    image: 'https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=300&h=200&fit=crop'
  },
  { 
    id: 4, 
    title: 'Data Analyst', 
    company: 'Analytics Co', 
    location: 'Los Angeles', 
    salary: '$85k+',
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=300&h=200&fit=crop'
  }
]
</script>
