<script setup>
import { ref } from 'vue'
import Home from './components/Home.vue'
import Mission from './components/Mission.vue'

// Simple state to track which page we're on
const currentPage = ref('home')

// Navigation functions
function showHome() { currentPage.value = 'home' }
function showMission() { currentPage.value = 'mission' }

// Placeholder functions for future components
function showBeneficiaries() { alert('Beneficiaries page coming soon!') }
function showAboutUs() { alert('About Us page coming soon!') }
function showGallery() { alert('Gallery page coming soon!') }
function showDonate() { alert('Donate page coming soon!') }
function showCovidRelief() { alert('Covid Relief page coming soon!') }
function showAmphanRelief() { alert('Amphan Relief page coming soon!') }
function showOtherRelief() { alert('Other Relief page coming soon!') }

// Mobile menu toggle
const isMobileMenuOpen = ref(false)
function toggleMobileMenu() {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navigation Header -->
    <header class="bg-gradient-to-r from-yellow-600 to-orange-600 shadow-lg sticky top-0 z-40 border-b-4 border-red-600">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center py-4">
          <!-- Logo Section -->
          <div class="flex items-center space-x-4">
            <div class="w-14 h-14 bg-white rounded-full flex items-center justify-center shadow-lg border-2 border-yellow-300 overflow-hidden">
              <img src="/logo.png" alt="Bidyangdehi Logo" class="w-10 h-10 object-contain">
            </div>
            <div>
              <h1 class="text-2xl font-bold text-white" style="font-family: 'Noto Sans Bengali', serif;">বিদ্যাঙ্গদেহী</h1>
              <p class="text-sm text-yellow-100">Educating Young Minds of Bengal</p>
            </div>
          </div>

          <!-- Desktop Navigation -->
          <nav class="hidden lg:flex items-center space-x-1">
            <button @click="showHome" :class="{ 'bg-white text-yellow-700 shadow-md': currentPage === 'home' }" 
              class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium border-2 border-transparent hover:border-yellow-300">
              Home
            </button>
            <button @click="showMission" :class="{ 'bg-white text-yellow-700 shadow-md': currentPage === 'mission' }" 
              class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium border-2 border-transparent hover:border-yellow-300">
              Mission
            </button>
            <button @click="showBeneficiaries" 
              class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium border-2 border-transparent hover:border-yellow-300">
              Beneficiaries
            </button>
            <button @click="showAboutUs" 
              class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium border-2 border-transparent hover:border-yellow-300">
              About Us
            </button>
            <button @click="showGallery" 
              class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium border-2 border-transparent hover:border-yellow-300">
              Gallery
            </button>
            
            <!-- Relief Programs Dropdown -->
            <div class="relative group">
              <button class="px-4 py-2 rounded-lg text-white hover:bg-white hover:text-yellow-700 transition-all font-medium flex items-center border-2 border-transparent hover:border-yellow-300">
                Relief Programs
                <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div class="absolute right-0 mt-2 w-48 bg-white rounded-lg shadow-xl opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-200 border-2 border-yellow-300">
                <button @click="showCovidRelief" class="block w-full text-left px-4 py-3 text-gray-700 hover:bg-yellow-50 hover:text-yellow-700 rounded-t-lg transition-colors">
                  Covid-19 Relief
                </button>
                <button @click="showAmphanRelief" class="block w-full text-left px-4 py-3 text-gray-700 hover:bg-yellow-50 hover:text-yellow-700 transition-colors">
                  Amphan Relief
                </button>
                <button @click="showOtherRelief" class="block w-full text-left px-4 py-3 text-gray-700 hover:bg-yellow-50 hover:text-yellow-700 rounded-b-lg transition-colors">
                  Other Relief
                </button>
              </div>
            </div>
            
            <button @click="showDonate" 
              class="px-8 py-3 bg-white text-red-600 rounded-full hover:bg-yellow-50 transition-all transform hover:scale-105 font-bold shadow-lg border-2 border-yellow-300 animate-pulse">
              🤝 Donate
            </button>
          </nav>

          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu" class="lg:hidden p-2 rounded-lg hover:bg-white hover:bg-opacity-20 text-white">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="isMobileMenuOpen" class="lg:hidden bg-white border-t-2 border-yellow-300">
        <div class="px-4 py-2 space-y-1">
          <button @click="showHome; toggleMobileMenu()" :class="{ 'bg-yellow-100 text-yellow-700': currentPage === 'home' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Home
          </button>
          <button @click="showMission; toggleMobileMenu()" :class="{ 'bg-yellow-100 text-yellow-700': currentPage === 'mission' }" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Mission
          </button>
          <button @click="showBeneficiaries; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Beneficiaries
          </button>
          <button @click="showAboutUs; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            About Us
          </button>
          <button @click="showGallery; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Gallery
          </button>
          <button @click="showCovidRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Covid-19 Relief
          </button>
          <button @click="showAmphanRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Amphan Relief
          </button>
          <button @click="showOtherRelief; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 rounded-lg text-gray-700 hover:bg-yellow-50 transition-colors">
            Other Relief
          </button>
          <button @click="showDonate; toggleMobileMenu()" 
            class="block w-full text-left px-4 py-3 bg-gradient-to-r from-yellow-500 to-orange-500 text-white rounded-lg hover:from-yellow-600 hover:to-orange-600 transition-colors font-bold">
            🤝 Donate Now
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
    </main>

    <!-- Footer -->
    <footer class="bg-gradient-to-r from-gray-800 to-gray-900 text-white py-12 border-t-4 border-yellow-600">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div>
            <div class="flex items-center space-x-3 mb-4">
              <div class="w-12 h-12 bg-gradient-to-br from-yellow-400 to-orange-500 rounded-full flex items-center justify-center overflow-hidden">
                <img src="/logo.png" alt="Bidyangdehi Logo" class="w-8 h-8 object-contain">
              </div>
              <h3 class="text-xl font-bold" style="font-family: 'Noto Sans Bengali', serif;">বিদ্যাঙ্গদেহী</h3>
            </div>
            <p class="text-gray-300 mb-4">বাংলার প্রতিটি শিশুর জীবনে শিক্ষার আলো পৌঁছে দেওয়াই আমাদের লক্ষ্য।</p>
            <p class="text-sm text-yellow-300">A not-for-profit 501(c)(3) organization</p>
            <p class="text-sm text-yellow-300">EIN/Tax ID: 86-2974017</p>
          </div>
          
          <div>
            <h4 class="text-lg font-semibold mb-4 text-yellow-300">Quick Links</h4>
            <div class="space-y-2">
              <button @click="showMission" class="block text-gray-300 hover:text-yellow-300 transition-colors">Mission</button>
              <button @click="showBeneficiaries" class="block text-gray-300 hover:text-yellow-300 transition-colors">Beneficiaries</button>
              <button @click="showGallery" class="block text-gray-300 hover:text-yellow-300 transition-colors">Gallery</button>
              <button @click="showDonate" class="block text-gray-300 hover:text-yellow-300 transition-colors font-semibold">🤝 Donate</button>
            </div>
          </div>
          
          <div>
            <h4 class="text-lg font-semibold mb-4 text-yellow-300">Relief Programs</h4>
            <div class="space-y-2">
              <button @click="showCovidRelief" class="block text-gray-300 hover:text-yellow-300 transition-colors">Covid-19 Relief</button>
              <button @click="showAmphanRelief" class="block text-gray-300 hover:text-yellow-300 transition-colors">Amphan Relief</button>
              <button @click="showOtherRelief" class="block text-gray-300 hover:text-yellow-300 transition-colors">Other Relief</button>
            </div>
          </div>
        </div>
        
        <div class="border-t border-gray-700 mt-8 pt-8 text-center">
          <p class="text-gray-400">&copy; 2025 Bidyangdehi. All rights reserved.</p>
          <p class="text-lg text-yellow-300 mt-2" style="font-family: 'Noto Sans Bengali', serif;">
            "শিক্ষাই জাতির মেরুদণ্ড"
          </p>
          <p class="text-sm text-gray-400 mt-1">
            "Education is the manifestation of the perfection already in man" - Swami Vivekananda
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
/* Import Bengali font */
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&display=swap');
</style>