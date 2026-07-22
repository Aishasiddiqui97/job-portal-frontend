<template>
  <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg transition-all">
    <div class="flex gap-4">
      <!-- Company Logo -->
      <div class="w-16 h-16 bg-gradient-to-br from-primary-100 to-primary-200 rounded-lg flex items-center justify-center text-3xl flex-shrink-0">
        {{ job.logo }}
      </div>

      <!-- Job Details -->
      <div class="flex-1">
        <h3 class="text-xl font-semibold text-gray-900 mb-2 hover:text-primary-600 cursor-pointer">
          {{ job.title }}
        </h3>
        <p class="text-gray-600 mb-3">
          {{ job.company }}
        </p>

        <!-- Description -->
        <p class="text-gray-600 text-sm mb-4 line-clamp-2">
          {{ job.description }}
        </p>

        <!-- Tags -->
        <div class="flex flex-wrap gap-2 mb-4">
          <span 
            v-for="tag in job.tags" 
            :key="tag"
            class="px-3 py-1 bg-gray-100 text-gray-700 text-xs rounded-full"
          >
            {{ tag }}
          </span>
        </div>

        <!-- Footer -->
        <div class="flex items-center justify-between">
          <div class="flex items-center gap-4 text-sm text-gray-600">
            <span class="flex items-center gap-1">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
              </svg>
              {{ job.location }}
            </span>
            <span class="text-primary-600 font-semibold">
              {{ job.salary }}
            </span>
          </div>
          <button @click="handleApply" class="btn-primary text-sm">
            Apply Now
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  job: Object
})

const handleApply = () => {
  console.log(`Applying for: ${props.job.title}`)
  alert(`Applying for ${props.job.title} at ${props.job.company}`)
}
</script>
