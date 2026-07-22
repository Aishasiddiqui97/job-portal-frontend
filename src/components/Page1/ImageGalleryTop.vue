<template>
  <!-- EXACT: Image Gallery from Page 1 Top -->
  <section class="bg-white px-4 py-4">
    <div class="max-w-6xl mx-auto">
      <!-- 2 Rows x 5 Columns Image Grid -->
      <div class="grid grid-cols-5 gap-2 mb-4">
        <!-- Row 1 -->
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/4299E1/ffffff?text=Job1" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/9F7AEA/ffffff?text=Job2" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/48BB78/ffffff?text=Job3" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/ED8936/ffffff?text=Job4" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden row-span-2">
          <!-- Large Featured Image -->
          <div class="relative w-full h-full">
            <img src="https://via.placeholder.com/200x310/2D3748/ffffff?text=Featured" class="w-full h-full object-cover" alt="Featured" />
            <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
              <p class="text-white text-sm font-semibold">Featured Job</p>
              <p class="text-white/80 text-xs">Click to explore</p>
            </div>
          </div>
        </div>
        
        <!-- Row 2 -->
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/F56565/ffffff?text=Job5" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/38B2AC/ffffff?text=Job6" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/ECC94B/ffffff?text=Job7" class="w-full h-full object-cover" alt="Job" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://via.placeholder.com/200x150/667EEA/ffffff?text=Job8" class="w-full h-full object-cover" alt="Job" />
        </div>
      </div>
    </div>
  </section>
</template>
