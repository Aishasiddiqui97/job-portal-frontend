<template>
  <!-- Company Logos Section - From Figma -->
  <section class="bg-white border-t border-gray-200 py-10">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Header -->
      <div class="text-center mb-8">
        <h2 class="text-xl font-semibold text-gray-900 mb-2">Trusted by Leading Companies</h2>
        <p class="text-gray-600">Join thousands of companies hiring on our platform</p>
      </div>

      <!-- Company Logos Grid -->
      <div class="grid grid-cols-3 md:grid-cols-6 gap-8 items-center">
        <div v-for="(company, index) in companies" :key="index"
             class="flex items-center justify-center grayscale hover:grayscale-0 transition-all opacity-60 hover:opacity-100">
          <div class="text-center">
            <div class="text-3xl mb-1">{{ company.logo }}</div>
            <p class="text-xs text-gray-600 font-medium">{{ company.name }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const companies = [
  { logo: '🚀', name: 'TechCorp' },
  { logo: '💼', name: 'BusinessHub' },
  { logo: '🎨', name: 'DesignCo' },
  { logo: '💻', name: 'CodeWorks' },
  { logo: '📱', name: 'AppDev' },
  { logo: '🏢', name: 'Enterprise' }
]
</script>
