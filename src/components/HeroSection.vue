<template>
  <!-- Hero Section with Image Gallery and Featured Job -->
  <section class="bg-gray-50 py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <!-- Heading -->
      <div class="mb-8">
        <h2 class="text-3xl font-bold text-gray-900 mb-2">
          Explore Open Positions
        </h2>
        <p class="text-gray-600">
          Browse through thousands of job opportunities
        </p>
      </div>

      <!-- Hero Grid: Images + Featured Job -->
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
        
        <!-- Left: Image Grid -->
        <div class="lg:col-span-2">
          <div class="grid grid-cols-3 gap-4">
            <div v-for="(img, idx) in images" :key="idx" class="aspect-video rounded-lg overflow-hidden">
              <img 
                :src="img" 
                :alt="`Job preview ${idx + 1}`"
                class="w-full h-full object-cover hover:scale-105 transition-transform duration-300"
              />
            </div>
          </div>
        </div>

        <!-- Right: Featured Job Card -->
        <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow">
          <div class="flex items-start gap-4 mb-4">
            <img 
              src="https://via.placeholder.com/80" 
              alt="Company"
              class="w-20 h-20 rounded-lg object-cover"
            />
            <div class="flex-1">
              <h3 class="font-semibold text-gray-900 mb-1">
                Senior UI/UX Designer
              </h3>
              <p class="text-sm text-gray-600">
                Google Inc.
              </p>
            </div>
          </div>
          
          <div class="space-y-2 mb-4">
            <div class="flex items-center gap-2 text-sm text-gray-600">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
              </svg>
              <span>San Francisco, CA</span>
            </div>
            <div class="flex items-center gap-2 text-sm text-gray-600">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
              <span>Full Time</span>
            </div>
          </div>

          <button class="w-full btn-primary">
            Apply Now
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const images = [
  'https://via.placeholder.com/300x200',
  'https://via.placeholder.com/300x200',
  'https://via.placeholder.com/300x200',
  'https://via.placeholder.com/300x200',
  'https://via.placeholder.com/300x200',
  'https://via.placeholder.com/300x200',
]
</script>
