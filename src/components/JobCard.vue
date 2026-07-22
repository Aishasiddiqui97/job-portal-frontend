<template>
  <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-xl transition-all cursor-pointer relative group">
    <!-- Bookmark Icon -->
    <button 
      @click.stop="toggleBookmark"
      class="absolute top-4 right-4 w-8 h-8 rounded-full hover:bg-gray-100 flex items-center justify-center transition-colors"
    >
      <svg 
        :class="[isBookmarked ? 'fill-primary-600 text-primary-600' : 'text-gray-400']"
        class="w-5 h-5" 
        fill="none" 
        stroke="currentColor" 
        viewBox="0 0 24 24"
      >
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 5a2 2 0 012-2h10a2 2 0 012 2v16l-7-3.5L5 21V5z"/>
      </svg>
    </button>

    <!-- Company Logo -->
    <div class="w-12 h-12 bg-gradient-to-br from-primary-100 to-primary-200 rounded-lg flex items-center justify-center text-2xl mb-4">
      {{ job.logo }}
    </div>

    <!-- Job Title -->
    <h3 class="text-lg font-semibold text-gray-900 mb-2 group-hover:text-primary-600">
      {{ job.title }}
    </h3>

    <!-- Company Name -->
    <p class="text-gray-600 text-sm mb-4">
      {{ job.company }}
    </p>

    <!-- Location & Salary -->
    <div class="flex items-center gap-4 mb-4 text-sm text-gray-600">
      <div class="flex items-center gap-1">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
        </svg>
        <span>{{ job.location }}</span>
      </div>
    </div>

    <div class="flex items-center gap-2 mb-4">
      <span class="text-primary-600 font-semibold text-sm">
        {{ job.salary }}
      </span>
    </div>

    <!-- Job Type Badge & Date -->
    <div class="flex items-center justify-between pt-4 border-t border-gray-100">
      <span :class="[
        'px-3 py-1 rounded-full text-xs font-medium',
        job.type === 'Remote' ? 'bg-green-100 text-green-700' : 'bg-blue-100 text-blue-700'
      ]">
        {{ job.type }}
      </span>
      <span class="text-xs text-gray-500">
        {{ job.postedDate }}
      </span>
    </div>

    <!-- Apply Button (Shows on Hover) -->
    <button @click.stop="handleApply" class="w-full mt-4 btn-primary opacity-0 group-hover:opacity-100 transition-opacity">
      Apply Now
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  job: Object
})

const isBookmarked = ref(false)

const toggleBookmark = () => {
  isBookmarked.value = !isBookmarked.value
  const action = isBookmarked.value ? 'added to' : 'removed from'
  console.log(`Job "${props.job.title}" ${action} bookmarks`)
  alert(`${props.job.title} has been ${action} your bookmarks!`)
}

const handleApply = () => {
  console.log(`Applying for: ${props.job.title} at ${props.job.company}`)
  alert(`Applying for ${props.job.title} position at ${props.job.company}`)
}
</script>
