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
            <img :src="`https://via.placeholder.com/240x135/${job.color}/ffffff?text=Job`" 
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
  { id: 1, title: 'Senior Designer', company: 'CompanyA', location: 'Remote', salary: '$90k', color: '4299E1' },
  { id: 2, title: 'Developer', company: 'CompanyB', location: 'SF', salary: '$110k', color: '9F7AEA' },
  { id: 3, title: 'Manager', company: 'CompanyC', location: 'NY', salary: '$100k', color: '48BB78' },
  { id: 4, title: 'Analyst', company: 'CompanyD', location: 'LA', salary: '$85k', color: 'ED8936' }
]
</script>
