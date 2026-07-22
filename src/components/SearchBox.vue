<template>
  <section class="bg-gradient-to-r from-primary-50 to-blue-50 py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-8">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
          Find Your Dream Job
        </h1>
        <p class="text-lg text-gray-600">
          Discover thousands of job opportunities from top companies
        </p>
      </div>

      <!-- Search Form -->
      <div class="bg-white rounded-lg shadow-lg p-6 max-w-5xl mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
          <!-- Keyword Input -->
          <div class="md:col-span-1">
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Keywords
            </label>
            <div class="relative">
              <input 
                v-model="searchKeyword"
                type="text" 
                placeholder="Job title, keywords..."
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent outline-none"
              />
              <svg class="absolute right-3 top-3.5 h-5 w-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/>
              </svg>
            </div>
          </div>

          <!-- Location Input -->
          <div class="md:col-span-1">
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Location
            </label>
            <div class="relative">
              <input 
                v-model="searchLocation"
                type="text" 
                placeholder="City or state"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent outline-none"
              />
              <svg class="absolute right-3 top-3.5 h-5 w-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
              </svg>
            </div>
          </div>

          <!-- Category Dropdown -->
          <div class="md:col-span-1">
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Category
            </label>
            <select 
              v-model="searchCategory"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent outline-none bg-white"
            >
              <option value="">All Categories</option>
              <option value="technology">Technology</option>
              <option value="marketing">Marketing</option>
              <option value="design">Design</option>
              <option value="sales">Sales</option>
              <option value="finance">Finance</option>
            </select>
          </div>

          <!-- Search Button -->
          <div class="md:col-span-1 flex items-end">
            <button @click="handleSearch" class="w-full btn-primary py-3">
              Search Jobs
            </button>
          </div>
        </div>
      </div>

      <!-- Popular Searches -->
      <div class="text-center mt-6">
        <p class="text-sm text-gray-600 mb-3">Popular Searches:</p>
        <div class="flex flex-wrap justify-center gap-2">
          <span @click="searchPopularTerm('Designer')" class="px-4 py-1.5 bg-white rounded-full text-sm text-gray-700 hover:bg-gray-50 cursor-pointer border border-gray-200 hover:border-primary-500 transition-colors">
            Designer
          </span>
          <span @click="searchPopularTerm('Developer')" class="px-4 py-1.5 bg-white rounded-full text-sm text-gray-700 hover:bg-gray-50 cursor-pointer border border-gray-200 hover:border-primary-500 transition-colors">
            Developer
          </span>
          <span @click="searchPopularTerm('Manager')" class="px-4 py-1.5 bg-white rounded-full text-sm text-gray-700 hover:bg-gray-50 cursor-pointer border border-gray-200 hover:border-primary-500 transition-colors">
            Manager
          </span>
          <span @click="searchPopularTerm('Marketing')" class="px-4 py-1.5 bg-white rounded-full text-sm text-gray-700 hover:bg-gray-50 cursor-pointer border border-gray-200 hover:border-primary-500 transition-colors">
            Marketing
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const searchKeyword = ref('')
const searchLocation = ref('')
const searchCategory = ref('')

const handleSearch = () => {
  console.log('Searching jobs with:', {
    keyword: searchKeyword.value,
    location: searchLocation.value,
    category: searchCategory.value
  })
  alert(`Searching for: ${searchKeyword.value || 'All Jobs'} in ${searchLocation.value || 'All Locations'}`)
}

const searchPopularTerm = (term) => {
  searchKeyword.value = term
  handleSearch()
}
</script>
