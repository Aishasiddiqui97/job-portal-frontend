<template>
  <!-- Job Listings - Long List from Figma Page 1 -->
  <section class="bg-white py-10">
    <div class="max-w-7xl mx-auto px-4">
      <!-- Header -->
      <div class="mb-6">
        <h2 class="text-2xl font-bold text-gray-900 mb-2">Recent Job Postings</h2>
        <p class="text-gray-600">{{ jobs.length }} jobs available</p>
      </div>

      <!-- Job List -->
      <div class="space-y-3">
        <div v-for="job in jobs" :key="job.id"
             class="bg-white border border-gray-200 rounded-lg p-4 hover:border-blue-500 hover:shadow-sm transition-all">
          <div class="flex items-start justify-between">
            <!-- Left: Job Info -->
            <div class="flex gap-4 flex-1">
              <!-- Logo -->
              <div class="w-12 h-12 bg-gray-100 rounded flex items-center justify-center flex-shrink-0">
                <span class="text-xl">{{ job.logo }}</span>
              </div>
              
              <!-- Details -->
              <div>
                <h3 class="font-semibold text-gray-900 mb-1">{{ job.title }}</h3>
                <p class="text-sm text-gray-600 mb-2">{{ job.company }} • {{ job.location }} • {{ job.type }}</p>
                <div class="flex gap-2">
                  <span v-for="tag in job.tags" :key="tag"
                        class="px-2 py-0.5 bg-gray-100 text-gray-600 text-xs rounded">
                    {{ tag }}
                  </span>
                </div>
              </div>
            </div>

            <!-- Right: Salary & Button -->
            <div class="text-right">
              <p class="font-bold text-blue-600 mb-2">{{ job.salary }}</p>
              <button class="px-4 py-1.5 bg-blue-600 text-white text-sm rounded hover:bg-blue-700 transition-colors">
                Apply
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  {
    id: 1,
    logo: '🏢',
    title: 'Senior Software Engineer',
    company: 'TechCorp',
    location: 'San Francisco',
    type: 'Full Time',
    salary: '$140k - $180k',
    tags: ['JavaScript', 'React', 'Node.js']
  },
  {
    id: 2,
    logo: '🎨',
    title: 'UI/UX Designer',
    company: 'DesignHub',
    location: 'Remote',
    type: 'Remote',
    salary: '$80k - $110k',
    tags: ['Figma', 'UI Design', 'Prototyping']
  },
  {
    id: 3,
    logo: '📱',
    title: 'Mobile Developer',
    company: 'AppWorks',
    location: 'Austin',
    type: 'Full Time',
    salary: '$100k - $130k',
    tags: ['React Native', 'iOS', 'Android']
  },
  {
    id: 4,
    logo: '💼',
    title: 'Product Manager',
    company: 'StartupXYZ',
    location: 'New York',
    type: 'Full Time',
    salary: '$120k - $150k',
    tags: ['Product Strategy', 'Agile', 'Leadership']
  }
]
</script>
