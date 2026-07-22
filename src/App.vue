<template>
  <div class="min-h-screen bg-white">
    <!-- Navbar -->
    <Navbar />
    
    <!-- Hero Section with Image Gallery (From Page 1) -->
    <HeroGallery />
    
    <!-- Feature Cards Section (From Page 2) -->
    <FeatureCards />
    
    <!-- Search Box -->
    <SearchBox />
    
    <!-- Job Categories with Icons (Merged from both pages) -->
    <JobCategories />
    
    <!-- Popular Categories (From Page 2) -->
    <PopularCategories />
    
    <!-- Featured Jobs Grid (From Page 2) -->
    <FeaturedJobs />
    
    <!-- Top Companies Hiring (From Page 2) -->
    <TopCompanies />
    
    <!-- Recent Job Openings (From Page 1) -->
    <RecentJobs />
    
    <!-- Blog/Articles Section (From Page 1) -->
    <BlogSection />
    
    <!-- Statistics/Info Section (From Page 2) -->
    <Statistics />
    
    <!-- Newsletter Section (From Page 2) -->
    <Newsletter />
    
    <!-- Company Logos (From Page 1) -->
    <FeaturedCompanies />
    
    <!-- Footer (Merged) -->
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import HeroGallery from './components/HeroGallery.vue'
import FeatureCards from './components/FeatureCards.vue'
import SearchBox from './components/SearchBox.vue'
import JobCategories from './components/JobCategories.vue'
import PopularCategories from './components/PopularCategories.vue'
import FeaturedJobs from './components/FeaturedJobs.vue'
import TopCompanies from './components/TopCompanies.vue'
import RecentJobs from './components/RecentJobs.vue'
import BlogSection from './components/BlogSection.vue'
import Statistics from './components/Statistics.vue'
import Newsletter from './components/Newsletter.vue'
import FeaturedCompanies from './components/FeaturedCompanies.vue'
import Footer from './components/Footer.vue'
</script>
