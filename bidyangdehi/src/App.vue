<script setup>
import { ref } from 'vue'
import Home from './components/Home.vue'
import Mission from './components/Mission.vue'
import Beneficiaries from './components/Beneficiaries.vue'
import AboutUs from './components/AboutUs.vue'
import Gallery from './components/Gallery.vue'
import Donate from './components/Donate.vue'
import CovidRelief from './components/CovidRelief.vue'
import AmphanRelief from './components/AmphanRelief.vue'
import OtherRelief from './components/OtherRelief.vue'

// Simple state to track which page we're on
const currentPage = ref('home')

// Navigation functions
function showHome() { currentPage.value = 'home' }
function showMission() { currentPage.value = 'mission' }
function showBeneficiaries() { currentPage.value = 'beneficiaries' }
function showAboutUs() { currentPage.value = 'about' }
function showGallery() { currentPage.value = 'gallery' }
function showDonate() { currentPage.value = 'donate' }
function showCovidRelief() { currentPage.value = 'covid' }
function showAmphanRelief() { currentPage.value = 'amphan' }
function showOtherRelief() { currentPage.value = 'other' }

// Mobile menu toggle
const isMobileMenuOpen = ref(false)
function toggleMobileMenu() {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navigation Header -->
    <header class="bg-white shadow-lg sticky top-0 z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center py-4">
          <!-- Logo Section -->
          <div class="flex items-center space-x-4">
            <div class="w-12 h-12 bg-gradient-to-br from-orange-400 to-green-500 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-lg">B</span>
            </div>
            <div>
              <h1 class="text-2xl font-bold text-gray-800">Bidyangdehi</h1>
              <p class="text-sm text-gray-600">Educating Young Minds of India</p>
            </div>
          </div>

          <!-- Desktop Navigation -->
          <nav class="hidden lg:flex space-x-1">
            <button @click="showHome" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'home' }" 
              class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium">
              Home
            </button>
            <button @click="showMission" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'mission' }" 
              class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium">
              Mission
            </button>
            <button @click="showBeneficiaries" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'beneficiaries' }" 
              class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium">
              Beneficiaries
            </button>
            <button @click="showAboutUs" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'about' }" 
              class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium">
              About Us
            </button>
            <button @click="showGallery" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'gallery' }" 
              class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium">
              Gallery
            </button>
            
            <!-- Relief Programs Dropdown -->
            <div class="relative group">
              <button class="px-4 py-2 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors font-medium flex items-center">
                Relief Programs
                <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div class="absolute right-0 mt-2 w-48 bg-white rounded-lg shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-200">
                <button @click="showCovidRelief" class="block w-full text-left px-4 py-2 text-gray-700 hover:bg-gray-50 rounded-t-lg">
                  Covid-19 Relief
                </button>
                <button @click="showAmphanRelief" class="block w-full text-left px-4 py-2 text-gray-700 hover:bg-gray-50">
                  Amphan Relief
                </button>
                <button @click="showOtherRelief" class="block w-full text-left px-4 py-2 text-gray-700 hover:bg-gray-50 rounded-b-lg">
                  Other Relief
                </button>
              </div>
            </div>
            
            <button @click="showDonate" 
              class="px-6 py-2 bg-gradient-to-r from-orange-500 to-red-500 text-white rounded-lg hover:from-orange-600 hover:to-red-600 transition-all transform hover:scale-105 font-medium">
              Donate
            </button>
          </nav>

          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu" class="lg:hidden p-2 rounded-lg hover:bg-gray-100">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="isMobileMenuOpen" class="lg:hidden bg-white border-t">
        <div class="px-4 py-2 space-y-1">
          <button @click="showHome; toggleMobileMenu()" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'home' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Home
          </button>
          <button @click="showMission; toggleMobileMenu()" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'mission' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Mission
          </button>
          <button @click="showBeneficiaries; toggleMobileMenu()" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'beneficiaries' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Beneficiaries
          </button>
          <button @click="showAboutUs; toggleMobileMenu()" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'about' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            About Us
          </button>
          <button @click="showGallery; toggleMobileMenu()" :class="{ 'bg-blue-100 text-blue-700': currentPage === 'gallery' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Gallery
          </button>
          <button @click="showCovidRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Covid-19 Relief
          </button>
          <button @click="showAmphanRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Amphan Relief
          </button>
          <button @click="showOtherRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-gray-100 transition-colors">
            Other Relief
          </button>
          <button @click="showDonate; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 bg-gradient-to-r from-orange-500 to-red-500 text-white rounded-lg hover:from-orange-600 hover:to-red-600 transition-colors">
            Donate
          </button>
        </div>
      </div>
    </header>

    <!-- Main Content Area -->
    <main class="flex-1">
      <!-- Page Components -->
      <Home v-if="currentPage === 'home'" 
        :show-mission="showMission"
        :show-donate="showDonate"
        :show-gallery="showGallery" />
      
      <Mission v-if="currentPage === 'mission'" 
        :show-home="showHome"
        :show-beneficiaries="showBeneficiaries" />
      
      <Beneficiaries v-if="currentPage === 'beneficiaries'" 
        :show-home="showHome"
        :show-mission="showMission" />
      
      <AboutUs v-if="currentPage === 'about'" 
        :show-home="showHome"
        :show-donate="showDonate" />
      
      <Gallery v-if="currentPage === 'gallery'" 
        :show-home="showHome"
        :show-donate="showDonate" />
      
      <Donate v-if="currentPage === 'donate'" 
        :show-home="showHome"
        :show-about="showAboutUs" />
      
      <CovidRelief v-if="currentPage === 'covid'" 
        :show-home="showHome"
        :show-donate="showDonate" />
      
      <AmphanRelief v-if="currentPage === 'amphan'" 
        :show-home="showHome"
        :show-donate="showDonate" />
      
      <OtherRelief v-if="currentPage === 'other'" 
        :show-home="showHome"
        :show-donate="showDonate" />
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div>
            <div class="flex items-center space-x-3 mb-4">
              <div class="w-10 h-10 bg-gradient-to-br from-orange-400 to-green-500 rounded-full flex items-center justify-center">
                <span class="text-white font-bold">B</span>
              </div>
              <h3 class="text-xl font-bold">Bidyangdehi</h3>
            </div>
            <p class="text-gray-300 mb-4">Educating young minds of India through quality education and relief programs.</p>
            <p class="text-sm text-gray-400">A not-for-profit 501(c)(3) organization</p>
            <p class="text-sm text-gray-400">EIN/Tax ID: 86-2974017</p>
          </div>
          
          <div>
            <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
            <div class="space-y-2">
              <button @click="showMission" class="block text-gray-300 hover:text-white transition-colors">Mission</button>
              <button @click="showBeneficiaries" class="block text-gray-300 hover:text-white transition-colors">Beneficiaries</button>
              <button @click="showGallery" class="block text-gray-300 hover:text-white transition-colors">Gallery</button>
              <button @click="showDonate" class="block text-gray-300 hover:text-white transition-colors">Donate</button>
            </div>
          </div>
          
          <div>
            <h4 class="text-lg font-semibold mb-4">Relief Programs</h4>
            <div class="space-y-2">
              <button @click="showCovidRelief" class="block text-gray-300 hover:text-white transition-colors">Covid-19 Relief</button>
              <button @click="showAmphanRelief" class="block text-gray-300 hover:text-white transition-colors">Amphan Relief</button>
              <button @click="showOtherRelief" class="block text-gray-300 hover:text-white transition-colors">Other Relief</button>
            </div>
          </div>
        </div>
        
        <div class="border-t border-gray-700 mt-8 pt-8 text-center">
          <p class="text-gray-400">&copy; 2025 Bidyangdehi. All rights reserved.</p>
          <p class="text-sm text-gray-500 mt-2">
            "Education is the manifestation of the perfection already in man" - Swami Vivekananda
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>