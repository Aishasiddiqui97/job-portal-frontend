<template>
  <!-- Featured Jobs - Compact Grid from Figma -->
  <section class="bg-gray-50 py-10">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Header -->
      <div class="flex justify-between items-center mb-6">
        <h2 class="text-2xl font-bold text-gray-900">Featured Jobs</h2>
        <a href="#" class="text-blue-600 text-sm font-medium hover:text-blue-700">View all →</a>
      </div>

      <!-- Jobs Grid - 3 Columns -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
        <div v-for="job in jobs" :key="job.id"
             class="bg-white border border-gray-200 rounded-lg p-4 hover:shadow-md transition-shadow">
          <!-- Company Logo -->
          <div class="w-10 h-10 bg-gradient-to-br from-blue-100 to-purple-100 rounded flex items-center justify-center mb-3">
            <span class="text-xl">{{ job.logo }}</span>
          </div>

          <!-- Job Title -->
          <h3 class="font-semibold text-gray-900 text-base mb-1">{{ job.title }}</h3>
          
          <!-- Company Name -->
          <p class="text-sm text-gray-600 mb-3">{{ job.company }}</p>

          <!-- Location & Salary -->
          <div class="flex items-center justify-between text-xs text-gray-500 mb-3">
            <span class="flex items-center gap-1">
              <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
              </svg>
              {{ job.location }}
            </span>
            <span class="font-semibold text-blue-600">{{ job.salary }}</span>
          </div>

          <!-- Tags -->
          <div class="flex gap-2 mb-3">
            <span class="px-2 py-1 bg-blue-50 text-blue-700 text-xs rounded">{{ job.type }}</span>
            <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">{{ job.level }}</span>
          </div>

          <!-- Posted Time -->
          <p class="text-xs text-gray-400">{{ job.posted }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  {
    id: 1,
    logo: '💼',
    title: 'Senior Product Designer',
    company: 'Google Inc.',
    location: 'California, USA',
    salary: '$120k - $150k',
    type: 'Full Time',
    level: 'Senior',
    posted: '2 days ago'
  },
  {
    id: 2,
    logo: '💻',
    title: 'Frontend Developer',
    company: 'Microsoft',
    location: 'Remote',
    salary: '$90k - $120k',
    type: 'Remote',
    level: 'Mid-Level',
    posted: '1 day ago'
  },
  {
    id: 3,
    logo: '📊',
    title: 'Marketing Manager',
    company: 'Amazon',
    location: 'New York, USA',
    salary: '$100k - $130k',
    type: 'Full Time',
    level: 'Manager',
    posted: '3 days ago'
  }
]
</script>
