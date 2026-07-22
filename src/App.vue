<template>
  <div class="min-h-screen bg-white">
    <!-- Navbar -->
    <Navbar />
    
    <!-- Page 1 Content - Jobs Without Filters -->
    <ImageGalleryTop />
    <CategoryIconsCircular />
    <JobCardsThreeColumn />
    <CategoryTagsPills />
    <BlogArticlesList />
    <TextContentSections />
    
    <!-- Page 2 Content - Desktop 137 -->
    <FeatureBoxesTop />
    <CategorySectionsWithIcons />
    <JobCardsFourColumn />
    <BlogArticlesWithImages />
    
    <!-- Footer -->
    <FooterMultiColumn />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import ImageGalleryTop from './components/Page1/ImageGalleryTop.vue'
import CategoryIconsCircular from './components/Page1/CategoryIconsCircular.vue'
import JobCardsThreeColumn from './components/Page1/JobCardsThreeColumn.vue'
import CategoryTagsPills from './components/Page1/CategoryTagsPills.vue'
import BlogArticlesList from './components/Page1/BlogArticlesList.vue'
import TextContentSections from './components/Page1/TextContentSections.vue'
import FeatureBoxesTop from './components/Page2/FeatureBoxesTop.vue'
import CategorySectionsWithIcons from './components/Page2/CategorySectionsWithIcons.vue'
import JobCardsFourColumn from './components/Page2/JobCardsFourColumn.vue'
import BlogArticlesWithImages from './components/Page2/BlogArticlesWithImages.vue'
import FooterMultiColumn from './components/FooterMultiColumn.vue'
</script>
