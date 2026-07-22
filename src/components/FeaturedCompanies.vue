<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-gray-900 mb-3">
          Featured Companies
        </h2>
        <p class="text-gray-600">
          Top companies hiring now
        </p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <CompanyCard 
          v-for="company in companies" 
          :key="company.id"
          :company="company"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import CompanyCard from './CompanyCard.vue'

const companies = [
  { id: 1, name: 'TechCorp', logo: '🚀', openPositions: 12 },
  { id: 2, name: 'Digital Inc', logo: '💼', openPositions: 8 },
  { id: 3, name: 'AI Systems', logo: '🤖', openPositions: 15 },
  { id: 4, name: 'Creative Co', logo: '🎨', openPositions: 6 },
  { id: 5, name: 'DataTech', logo: '📊', openPositions: 10 },
  { id: 6, name: 'CloudBase', logo: '☁️', openPositions: 9 },
  { id: 7, name: 'WebSolutions', logo: '🌐', openPositions: 7 },
  { id: 8, name: 'DevHub', logo: '💻', openPositions: 11 }
]
</script>
