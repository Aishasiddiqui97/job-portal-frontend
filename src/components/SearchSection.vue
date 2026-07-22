<template>
  <!-- Search Section - From Figma -->
  <section class="bg-white border-b border-gray-200 py-6">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Search Form -->
      <div class="bg-white border border-gray-300 rounded-lg p-4 shadow-sm">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
          <!-- Keyword Input -->
          <div class="relative">
            <input 
              type="text" 
              placeholder="Keywords" 
              class="w-full px-4 py-2.5 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 text-sm"
            />
          </div>

          <!-- Location Input -->
          <div class="relative">
            <input 
              type="text" 
              placeholder="Location" 
              class="w-full px-4 py-2.5 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 text-sm"
            />
          </div>

          <!-- Category Dropdown -->
          <div class="relative">
            <select class="w-full px-4 py-2.5 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 text-sm bg-white">
              <option>All Categories</option>
              <option>Technology</option>
              <option>Marketing</option>
              <option>Design</option>
              <option>Sales</option>
            </select>
          </div>

          <!-- Search Button -->
          <button class="bg-blue-600 text-white px-6 py-2.5 rounded-md hover:bg-blue-700 transition-colors font-medium text-sm">
            Search Jobs
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
