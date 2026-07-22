<template>
  <div class="bg-white border border-gray-200 rounded-xl p-6 sticky top-24">
    <h3 class="text-xl font-bold text-gray-900 mb-6">
      Filter Jobs
    </h3>

    <!-- Job Type Filter -->
    <div class="mb-8">
      <h4 class="font-semibold text-gray-900 mb-4">Job Type</h4>
      <div class="space-y-3">
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Full Time</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Part Time</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Remote</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Contract</span>
        </label>
      </div>
    </div>

    <!-- Salary Range Filter -->
    <div class="mb-8">
      <h4 class="font-semibold text-gray-900 mb-4">Salary Range</h4>
      <div class="space-y-3">
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">$0 - $50k</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">$50k - $100k</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">$100k - $150k</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">$150k+</span>
        </label>
      </div>
    </div>

    <!-- Experience Level Filter -->
    <div class="mb-8">
      <h4 class="font-semibold text-gray-900 mb-4">Experience Level</h4>
      <div class="space-y-3">
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Entry Level</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Mid Level</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Senior Level</span>
        </label>
        <label class="flex items-center cursor-pointer">
          <input type="checkbox" class="w-4 h-4 text-primary-600 rounded focus:ring-primary-500" />
          <span class="ml-3 text-gray-700">Executive</span>
        </label>
      </div>
    </div>

    <!-- Apply Filters Button -->
    <button @click="applyFilters" class="w-full btn-primary">
      Apply Filters
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const applyFilters = () => {
  console.log('Applying filters...')
  alert('Filters applied! Job listings will be updated.')
}
</script>
