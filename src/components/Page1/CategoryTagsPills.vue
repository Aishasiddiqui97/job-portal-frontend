<template>
  <!-- EXACT: Horizontal Tag Pills from Page 1 -->
  <section class="bg-white px-4 py-4 border-y border-gray-200">
    <div class="max-w-6xl mx-auto">
      <p class="text-xs text-gray-600 mb-2">Popular Categories:</p>
      <div class="flex flex-wrap gap-2">
        <button v-for="tag in tags" :key="tag"
                class="px-3 py-1 bg-gray-100 hover:bg-blue-50 text-gray-700 hover:text-blue-600 text-xs rounded-full border border-gray-200 transition">
          {{ tag }}
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const tags = ['Design', 'Development', 'Marketing', 'Finance', 'Sales', 'Support', 'HR', 'Legal']
</script>
