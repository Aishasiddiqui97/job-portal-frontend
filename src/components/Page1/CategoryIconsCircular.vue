<template>
  <!-- EXACT: Circular Category Icons from Page 1 -->
  <section class="bg-white px-4 py-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-lg font-bold text-gray-900 mb-4">Browse by Category</h2>
      
      <!-- 3 Rows x 3 Columns of Circular Icons -->
      <div class="grid grid-cols-3 gap-6">
        <div v-for="icon in icons" :key="icon.id" class="flex flex-col items-center">
          <!-- Circular Icon -->
          <div :class="['w-14 h-14 rounded-full flex items-center justify-center mb-2', icon.bg]">
            <span class="text-2xl">{{ icon.emoji }}</span>
          </div>
          <!-- Label -->
          <span class="text-xs text-gray-700 text-center">{{ icon.label }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const icons = [
  { id: 1, emoji: '🏢', label: 'Corporate', bg: 'bg-blue-100' },
  { id: 2, emoji: '🎯', label: 'Marketing', bg: 'bg-green-100' },
  { id: 3, emoji: '💻', label: 'Tech', bg: 'bg-purple-100' },
  { id: 4, emoji: '📱', label: 'Mobile', bg: 'bg-pink-100' },
  { id: 5, emoji: '🎨', label: 'Design', bg: 'bg-yellow-100' },
  { id: 6, emoji: '📊', label: 'Analytics', bg: 'bg-red-100' },
  { id: 7, emoji: '⚙️', label: 'Engineering', bg: 'bg-gray-100' },
  { id: 8, emoji: '🚀', label: 'Startup', bg: 'bg-indigo-100' },
  { id: 9, emoji: '💼', label: 'Business', bg: 'bg-teal-100' }
]
</script>
