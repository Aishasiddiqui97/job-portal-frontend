<template>
  <!-- Top Companies Hiring (From Figma Page 2) -->
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center mb-12">
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-2">
            Top Companies Hiring
          </h2>
          <p class="text-gray-600">
            Explore opportunities at leading companies
          </p>
        </div>
        <button class="text-blue-600 font-medium hover:text-blue-700 flex items-center gap-2">
          View All Companies
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
        <div v-for="(company, index) in companies" :key="index"
             class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-blue-500 transition-all group cursor-pointer">
          <!-- Company Logo -->
          <div class="w-16 h-16 bg-gradient-to-br from-blue-50 to-purple-50 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-3xl">{{ company.logo }}</span>
          </div>
          
          <!-- Company Name -->
          <h3 class="font-semibold text-gray-900 mb-1 text-sm">
            {{ company.name }}
          </h3>
          
          <!-- Jobs Count -->
          <p class="text-xs text-gray-600">
            {{ company.jobs }} open jobs
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const companies = [
  { logo: '🚀', name: 'TechCorp', jobs: 25 },
  { logo: '💼', name: 'BusinessHub', jobs: 18 },
  { logo: '🎨', name: 'DesignStudio', jobs: 12 },
  { logo: '💻', name: 'CodeLabs', jobs: 30 },
  { logo: '📱', name: 'AppWorks', jobs: 15 },
  { logo: '🏢', name: 'Enterprise Co', jobs: 22 },
  { logo: '🌐', name: 'WebSolutions', jobs: 14 },
  { logo: '📊', name: 'DataTech', jobs: 19 },
  { logo: '⚡', name: 'QuickStart', jobs: 11 },
  { logo: '🎯', name: 'TargetCorp', jobs: 16 },
  { logo: '🔧', name: 'BuildIt', jobs: 13 },
  { logo: '💡', name: 'Innovation Labs', jobs: 20 }
]
</script>
