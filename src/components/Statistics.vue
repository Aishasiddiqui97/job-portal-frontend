<template>
  <!-- Statistics Section (From Figma Page 2) -->
  <section class="py-20 bg-gradient-to-br from-blue-600 to-purple-600 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold mb-4">
          Trusted by Thousands
        </h2>
        <p class="text-blue-100 text-lg">
          Join the community of successful job seekers
        </p>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
        <div v-for="(stat, index) in stats" :key="index" class="text-center">
          <div class="text-5xl font-bold mb-2">
            {{ stat.value }}
          </div>
          <div class="text-blue-100">
            {{ stat.label }}
          </div>
        </div>
      </div>

      <!-- CTA -->
      <div class="text-center mt-16">
        <button class="bg-white text-blue-600 px-8 py-4 rounded-lg font-semibold hover:bg-gray-100 transition-colors text-lg">
          Start Your Journey Today
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { value: '10,000+', label: 'Active Jobs' },
  { value: '5,000+', label: 'Companies' },
  { value: '8,000+', label: 'Candidates' },
  { value: '95%', label: 'Success Rate' }
]
</script>
