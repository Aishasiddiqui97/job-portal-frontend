<template>
  <div class="min-h-screen bg-gray-50">
    <Navbar />
    <SearchBox />
    <JobCategories />
    <FeaturedJobs />
    <JobListingSection />
    <FeaturedCompanies />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import SearchBox from './components/SearchBox.vue'
import JobCategories from './components/JobCategories.vue'
import FeaturedJobs from './components/FeaturedJobs.vue'
import JobListingSection from './components/JobListingSection.vue'
import FeaturedCompanies from './components/FeaturedCompanies.vue'
import Footer from './components/Footer.vue'
</script>
