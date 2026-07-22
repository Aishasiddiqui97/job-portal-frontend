<template>
  <section class="py-16 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
        <!-- Main Job Listing Area -->
        <div class="lg:col-span-2">
          <div class="mb-8">
            <h2 class="text-3xl font-bold text-gray-900 mb-2">
              Recent Job Openings
            </h2>
            <p class="text-gray-600">
              {{ jobListings.length }} jobs found
            </p>
          </div>

          <div class="space-y-6">
            <JobListingCard 
              v-for="job in jobListings" 
              :key="job.id"
              :job="job"
            />
          </div>
        </div>

        <!-- Sidebar Filters -->
        <div class="lg:col-span-1">
          <Sidebar />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import JobListingCard from './JobListingCard.vue'
import Sidebar from './Sidebar.vue'

const jobListings = [
  {
    id: 1,
    title: 'Full Stack Web Developer',
    company: 'WebTech Solutions',
    location: 'Seattle, WA',
    salary: '$95k - $125k',
    type: 'Full Time',
    logo: '🌐',
    description: 'Looking for an experienced full stack developer to join our team...',
    tags: ['JavaScript', 'React', 'Node.js', 'MongoDB']
  },
  {
    id: 2,
    title: 'UX/UI Designer',
    company: 'Creative Studio',
    location: 'Los Angeles, CA',
    salary: '$85k - $110k',
    type: 'Remote',
    logo: '🎨',
    description: 'We are seeking a talented UX/UI designer with experience in...',
    tags: ['Figma', 'Adobe XD', 'User Research', 'Prototyping']
  },
  {
    id: 3,
    title: 'DevOps Engineer',
    company: 'Cloud Systems',
    location: 'Austin, TX',
    salary: '$115k - $145k',
    type: 'Full Time',
    logo: '☁️',
    description: 'Join our infrastructure team to build scalable cloud solutions...',
    tags: ['AWS', 'Docker', 'Kubernetes', 'CI/CD']
  }
]
</script>
