<template>
  <!-- Recent Job Openings (From Figma Page 1 - Long List) -->
  <section class="py-16 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="mb-12">
        <h2 class="text-3xl font-bold text-gray-900 mb-2">
          Recent Job Openings
        </h2>
        <p class="text-gray-600">
          {{ jobs.length }} new jobs posted this week
        </p>
      </div>

      <div class="space-y-4">
        <div v-for="job in jobs" :key="job.id"
             class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg transition-all hover:border-blue-500">
          <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
            <!-- Left: Job Info -->
            <div class="flex gap-4 flex-1">
              <!-- Company Logo -->
              <div class="w-12 h-12 bg-gradient-to-br from-blue-100 to-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
                <span class="text-xl">{{ job.logo }}</span>
              </div>
              
              <!-- Job Details -->
              <div class="flex-1">
                <h3 class="text-lg font-semibold text-gray-900 mb-1 hover:text-blue-600 cursor-pointer">
                  {{ job.title }}
                </h3>
                <div class="flex flex-wrap items-center gap-3 text-sm text-gray-600">
                  <span class="flex items-center gap-1">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
                    </svg>
                    {{ job.company }}
                  </span>
                  <span class="flex items-center gap-1">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                    </svg>
                    {{ job.location }}
                  </span>
                  <span class="flex items-center gap-1">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
                    </svg>
                    {{ job.type }}
                  </span>
                </div>
                
                <!-- Tags -->
                <div class="flex flex-wrap gap-2 mt-3">
                  <span v-for="tag in job.tags" :key="tag"
                        class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded-md">
                    {{ tag }}
                  </span>
                </div>
              </div>
            </div>

            <!-- Right: Salary & Actions -->
            <div class="flex md:flex-col items-center md:items-end gap-3">
              <div class="text-right">
                <div class="text-lg font-bold text-blue-600">{{ job.salary }}</div>
                <div class="text-xs text-gray-500">{{ job.posted }}</div>
              </div>
              <button class="btn-primary text-sm px-6 py-2">
                Apply Now
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Load More -->
      <div class="text-center mt-8">
        <button class="btn-secondary px-8 py-3">
          Load More Jobs
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  {
    id: 1,
    title: 'Senior Frontend Developer',
    company: 'TechCorp Inc',
    location: 'San Francisco, CA',
    type: 'Full Time',
    salary: '$120k - $150k',
    posted: '2 days ago',
    logo: '💻',
    tags: ['React', 'TypeScript', 'Tailwind CSS']
  },
  {
    id: 2,
    title: 'Product Designer',
    company: 'Design Studio',
    location: 'Remote',
    type: 'Remote',
    salary: '$90k - $120k',
    posted: '1 day ago',
    logo: '🎨',
    tags: ['Figma', 'UI/UX', 'Prototyping']
  },
  {
    id: 3,
    title: 'Marketing Manager',
    company: 'Growth Agency',
    location: 'New York, NY',
    type: 'Full Time',
    salary: '$100k - $130k',
    posted: '3 days ago',
    logo: '📊',
    tags: ['SEO', 'Content', 'Analytics']
  },
  {
    id: 4,
    title: 'Data Scientist',
    company: 'AI Solutions',
    location: 'Boston, MA',
    type: 'Full Time',
    salary: '$130k - $160k',
    posted: '5 days ago',
    logo: '🤖',
    tags: ['Python', 'Machine Learning', 'SQL']
  },
  {
    id: 5,
    title: 'DevOps Engineer',
    company: 'Cloud Systems',
    location: 'Austin, TX',
    type: 'Full Time',
    salary: '$110k - $140k',
    posted: '1 week ago',
    logo: '☁️',
    tags: ['AWS', 'Docker', 'Kubernetes']
  }
]
</script>
