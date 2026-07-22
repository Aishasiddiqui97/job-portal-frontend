<template>
  <!-- Feature Cards Section (From Figma Page 2) -->
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-gray-900 mb-3">
          How It Works
        </h2>
        <p class="text-gray-600 text-lg">
          Get hired in 4 quick easy steps
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div v-for="(feature, index) in features" :key="index"
             class="bg-white border border-gray-200 rounded-2xl p-6 hover:shadow-xl transition-all hover:border-blue-500 group">
          <!-- Icon -->
          <div class="w-14 h-14 bg-gradient-to-br from-blue-100 to-blue-200 rounded-xl flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
            <span class="text-2xl">{{ feature.icon }}</span>
          </div>
          
          <!-- Step Number -->
          <div class="inline-block px-3 py-1 bg-gray-100 text-gray-700 rounded-full text-xs font-semibold mb-3">
            Step {{ index + 1 }}
          </div>
          
          <!-- Title -->
          <h3 class="text-xl font-semibold text-gray-900 mb-2">
            {{ feature.title }}
          </h3>
          
          <!-- Description -->
          <p class="text-gray-600 text-sm leading-relaxed">
            {{ feature.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: '👤',
    title: 'Create Account',
    description: 'Sign up and create your professional profile in minutes'
  },
  {
    icon: '🔍',
    title: 'Search Jobs',
    description: 'Browse through thousands of job listings from top companies'
  },
  {
    icon: '📄',
    title: 'Apply for Jobs',
    description: 'Submit your application with just one click'
  },
  {
    icon: '🎉',
    title: 'Get Hired',
    description: 'Connect with employers and land your dream job'
  }
]
</script>
