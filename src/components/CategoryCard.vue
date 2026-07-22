<template>
  <div @click="handleCategoryClick" class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-primary-500 transition-all cursor-pointer group">
    <div :class="[color, 'w-14 h-14 rounded-lg flex items-center justify-center mb-4 text-2xl group-hover:scale-110 transition-transform']">
      {{ icon }}
    </div>
    <h3 class="text-lg font-semibold text-gray-900 mb-2 group-hover:text-primary-600">
      {{ title }}
    </h3>
    <p class="text-gray-600 text-sm">
      {{ count }} open positions
    </p>
  </div>
</template>

<script setup>
const props = defineProps({
  icon: String,
  title: String,
  count: Number,
  color: String
})

const handleCategoryClick = () => {
  console.log(`Browsing ${props.title} category`)
  alert(`Viewing ${props.count} jobs in ${props.title}`)
}
</script>
