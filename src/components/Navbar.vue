<template>
  <nav class="bg-white shadow-sm border-b border-gray-200 sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex items-center">
          <div class="text-2xl font-bold text-primary-600">
            iKjobs
          </div>
        </div>

        <!-- Navigation Links -->
        <div class="hidden md:flex items-center space-x-8">
          <a href="#" class="text-gray-900 font-medium hover:text-primary-600 transition-colors">
            Home
          </a>
          <a href="#" class="text-gray-600 hover:text-primary-600 transition-colors">
            Find Jobs
          </a>
          <a href="#" class="text-gray-600 hover:text-primary-600 transition-colors">
            Companies
          </a>
          <a href="#" class="text-gray-600 hover:text-primary-600 transition-colors">
            Candidates
          </a>
          <a href="#" class="text-gray-600 hover:text-primary-600 transition-colors">
            Industries
          </a>
          <a href="#" class="text-gray-600 hover:text-primary-600 transition-colors">
            Articles
          </a>
        </div>

        <!-- Right Side Buttons -->
        <div class="hidden md:flex items-center space-x-4">
          <button @click="handleLogin" class="text-gray-700 font-medium hover:text-primary-600 transition-colors">
            Login
          </button>
          <button @click="handlePostJob" class="btn-accent">
            Post A Job
          </button>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-600 hover:text-gray-900">
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <div v-if="mobileMenuOpen" class="md:hidden py-4 border-t border-gray-200">
        <div class="flex flex-col space-y-3">
          <a href="#" class="text-gray-900 font-medium">Home</a>
          <a href="#" class="text-gray-600">Find Jobs</a>
          <a href="#" class="text-gray-600">Companies</a>
          <a href="#" class="text-gray-600">Candidates</a>
          <a href="#" class="text-gray-600">Industries</a>
          <a href="#" class="text-gray-600">Articles</a>
          <button @click="handleLogin" class="btn-secondary text-left">Login</button>
          <button @click="handlePostJob" class="btn-accent">Post A Job</button>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const handleLogin = () => {
  alert('Login functionality would redirect to login page')
  console.log('Redirecting to login...')
}

const handlePostJob = () => {
  alert('Post Job functionality would redirect to employer dashboard')
  console.log('Redirecting to post job...')
}
</script>
