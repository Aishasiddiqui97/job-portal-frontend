<template>
  <!-- EXACT: Image Gallery from Page 1 Top -->
  <section class="bg-white px-4 py-4">
    <div class="max-w-6xl mx-auto">
      <!-- 2 Rows x 5 Columns Image Grid with Real Images -->
      <div class="grid grid-cols-5 gap-2 mb-4">
        <!-- Row 1 -->
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Office Work" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Team Meeting" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1553877522-43269d4ea984?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Business Meeting" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Office Space" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden row-span-2">
          <!-- Large Featured Image -->
          <div class="relative w-full h-full">
            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?w=400&h=600&fit=crop" class="w-full h-full object-cover" alt="Professional Woman" />
            <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
              <p class="text-white text-sm font-semibold">Featured Job</p>
              <p class="text-white/80 text-xs">Join our team today</p>
            </div>
          </div>
        </div>
        
        <!-- Row 2 -->
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Modern Office" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Office Discussion" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1557804506-669a67965ba0?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Team Collaboration" />
        </div>
        <div class="aspect-[4/3] bg-gray-200 rounded overflow-hidden">
          <img src="https://images.unsplash.com/photo-1556761175-4b46a572b786?w=400&h=300&fit=crop" class="w-full h-full object-cover" alt="Office Environment" />
        </div>
      </div>
    </div>
  </section>
</template>
