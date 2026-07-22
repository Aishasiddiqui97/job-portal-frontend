<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center mb-12">
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-3">
            Featured Jobs
          </h2>
          <p class="text-gray-600">
            Top job picks handpicked for you
          </p>
        </div>
        <button class="text-primary-600 font-medium hover:text-primary-700 flex items-center gap-2">
          View All
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <JobCard 
          v-for="job in featuredJobs" 
          :key="job.id"
          :job="job"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import JobCard from './JobCard.vue'

const featuredJobs = [
  {
    id: 1,
    title: 'Senior Product Designer',
    company: 'TechCorp Inc',
    location: 'San Francisco, CA',
    salary: '$120k - $150k',
    type: 'Full Time',
    postedDate: '2 days ago',
    logo: '🚀',
    featured: true
  },
  {
    id: 2,
    title: 'Frontend Developer',
    company: 'Digital Solutions',
    location: 'Remote',
    salary: '$90k - $120k',
    type: 'Remote',
    postedDate: '1 day ago',
    logo: '💡',
    featured: true
  },
  {
    id: 3,
    title: 'Marketing Manager',
    company: 'Growth Agency',
    location: 'New York, NY',
    salary: '$100k - $130k',
    type: 'Full Time',
    postedDate: '3 days ago',
    logo: '📊',
    featured: true
  },
  {
    id: 4,
    title: 'Data Scientist',
    company: 'AI Innovations',
    location: 'Boston, MA',
    salary: '$130k - $160k',
    type: 'Full Time',
    postedDate: '1 week ago',
    logo: '🤖',
    featured: true
  }
]
</script>
