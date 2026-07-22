<template>
  <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg transition-all text-center group">
    <div class="w-16 h-16 bg-gradient-to-br from-primary-100 to-primary-200 rounded-full flex items-center justify-center text-3xl mx-auto mb-4 group-hover:scale-110 transition-transform">
      {{ company.logo }}
    </div>
    <h3 class="text-lg font-semibold text-gray-900 mb-2">
      {{ company.name }}
    </h3>
    <p class="text-gray-600 text-sm mb-4">
      {{ company.openPositions }} open positions
    </p>
    <button @click="handleViewJobs" class="w-full btn-secondary text-sm">
      View Jobs
    </button>
  </div>
</template>

<script setup>
const props = defineProps({
  company: Object
})

const handleViewJobs = () => {
  console.log(`Viewing jobs at ${props.company.name}`)
  alert(`Showing ${props.company.openPositions} open positions at ${props.company.name}`)
}
</script>
