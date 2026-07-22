<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navbar - Exact from Figma -->
    <Navbar />
    
    <!-- Main Content -->
    <main>
      <!-- Hero Section with Images - Figma Page 1 Top -->
      <HeroWithImages />
      
      <!-- Search Bar Section -->
      <SearchSection />
      
      <!-- Job Categories with Icons Grid -->
      <CategoryGrid />
      
      <!-- Featured Jobs Section -->
      <FeaturedJobsGrid />
      
      <!-- Recent Job Listings -->
      <JobListings />
      
      <!-- Blog Articles Section -->
      <BlogArticles />
      
      <!-- Company Logos -->
      <CompanyLogos />
    </main>
    
    <!-- Footer -->
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import HeroWithImages from './components/HeroWithImages.vue'
import SearchSection from './components/SearchSection.vue'
import CategoryGrid from './components/CategoryGrid.vue'
import FeaturedJobsGrid from './components/FeaturedJobsGrid.vue'
import JobListings from './components/JobListings.vue'
import BlogArticles from './components/BlogArticles.vue'
import CompanyLogos from './components/CompanyLogos.vue'
import Footer from './components/Footer.vue'
</script>
