<script setup>
// Props to receive navigation functions from parent
defineProps({
  showMission: Function,
  showDonate: Function,
  showGallery: Function
})
</script>

<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="relative bg-gradient-to-br from-blue-600 via-purple-600 to-green-500 text-white py-20 overflow-hidden">
      <div class="absolute inset-0 bg-black opacity-20"></div>
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div class="text-center lg:text-left">
            <h1 class="text-5xl lg:text-6xl font-bold mb-6 leading-tight">
              Educating
              <span class="block text-yellow-300">Young Minds</span>
              <span class="block text-green-300">of India</span>
            </h1>
            <p class="text-xl mb-8 text-blue-100">
              Empowering communities through education, relief programs, and sustainable development initiatives across India.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
              <button @click="showMission" 
                class="px-8 py-4 bg-white text-blue-600 rounded-full font-semibold hover:bg-blue-50 transform hover:scale-105 transition-all duration-200 shadow-lg">
                Our Mission
              </button>
              <button @click="showDonate" 
                class="px-8 py-4 bg-gradient-to-r from-orange-500 to-red-500 text-white rounded-full font-semibold hover:from-orange-600 hover:to-red-600 transform hover:scale-105 transition-all duration-200 shadow-lg">
                Donate Now
              </button>
            </div>
          </div>
          
          <div class="relative">
            <div class="w-80 h-80 mx-auto bg-white bg-opacity-10 rounded-full flex items-center justify-center backdrop-blur-sm">
              <div class="w-64 h-64 bg-gradient-to-br from-yellow-400 to-green-500 rounded-full flex items-center justify-center shadow-2xl">
                <svg class="w-32 h-32 text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 3L1 9l4 2.18v6L12 21l7-3.82v-6l2-1.09V17h2V9L12 3zm6.82 6L12 12.72 5.18 9 12 5.28 18.82 9zM17 15.99l-5 2.73-5-2.73v-3.72L12 15l5-2.73v3.72z"/>
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="py-16 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8 text-center">
          <div class="p-6">
            <div class="text-4xl font-bold text-blue-600 mb-2">1000+</div>
            <div class="text-gray-600">Students Educated</div>
          </div>
          <div class="p-6">
            <div class="text-4xl font-bold text-green-600 mb-2">50+</div>
            <div class="text-gray-600">Villages Reached</div>
          </div>
          <div class="p-6">
            <div class="text-4xl font-bold text-purple-600 mb-2">25+</div>
            <div class="text-gray-600">Relief Programs</div>
          </div>
          <div class="p-6">
            <div class="text-4xl font-bold text-orange-600 mb-2">5000+</div>
            <div class="text-gray-600">Lives Impacted</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Mission Preview -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-800 mb-4">Our Impact</h2>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Through education and community support, we're building a brighter future for India's next generation.
          </p>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <!-- Education Card -->
          <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow duration-300">
            <div class="h-48 bg-gradient-to-br from-blue-400 to-blue-600 flex items-center justify-center">
              <svg class="w-16 h-16 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 3L1 9l4 2.18v6L12 21l7-3.82v-6l2-1.09V17h2V9L12 3zm6.82 6L12 12.72 5.18 9 12 5.28 18.82 9zM17 15.99l-5 2.73-5-2.73v-3.72L12 15l5-2.73v3.72z"/>
              </svg>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-gray-800 mb-3">Quality Education</h3>
              <p class="text-gray-600 mb-4">Providing access to quality education for underprivileged children in rural and urban areas.</p>
              <button @click="showMission" class="text-blue-600 font-semibold hover:text-blue-700 transition-colors">
                Learn More →
              </button>
            </div>
          </div>

          <!-- Relief Programs Card -->
          <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow duration-300">
            <div class="h-48 bg-gradient-to-br from-green-400 to-green-600 flex items-center justify-center">
              <svg class="w-16 h-16 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
              </svg>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-gray-800 mb-3">Relief Programs</h3>
              <p class="text-gray-600 mb-4">Emergency relief and support during natural disasters and health crises like COVID-19.</p>
              <button @click="showMission" class="text-green-600 font-semibold hover:text-green-700 transition-colors">
                Learn More →
              </button>
            </div>
          </div>

          <!-- Community Development Card -->
          <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow duration-300">
            <div class="h-48 bg-gradient-to-br from-purple-400 to-purple-600 flex items-center justify-center">
              <svg class="w-16 h-16 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M16 4c0-1.11.89-2 2-2s2 .89 2 2-.89 2-2 2-2-.89-2-2zm4 18v-6h2.5l-2.54-7.63A2.998 2.998 0 0 0 17.11 7H14.5c-.83 0-1.5.67-1.5 1.5S13.67 10 14.5 10H16l1.8 5.4L16 17v5h4zM12.5 11.5c.83 0 1.5-.67 1.5-1.5s-.67-1.5-1.5-1.5S11 9.17 11 10s.67 1.5 1.5 1.5zm1.5 1h-4c-.83 0-1.5.67-1.5 1.5S9.17 15 10 15h1l1.8 5.4L11 22h4v-5l-1.8-2L15 13.5z"/>
              </svg>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-gray-800 mb-3">Community Building</h3>
              <p class="text-gray-600 mb-4">Strengthening communities through sustainable development and empowerment programs.</p>
              <button @click="showMission" class="text-purple-600 font-semibold hover:text-purple-700 transition-colors">
                Learn More →
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Quote Section -->
    <section class="py-20 bg-gradient-to-r from-gray-800 to-gray-900 text-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <blockquote class="text-3xl lg:text-4xl font-light italic mb-8 leading-relaxed">
          "Education is the manifestation of the perfection already in man"
        </blockquote>
        <cite class="text-xl text-gray-300">— Swami Vivekananda</cite>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-20 bg-gradient-to-br from-orange-400 to-red-500 text-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-4xl font-bold mb-6">Join Our Mission</h2>
        <p class="text-xl mb-8 opacity-90">
          Your support can help us reach more children and communities across India. 
          Together, we can build a brighter future through education.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button @click="showDonate" 
            class="px-8 py-4 bg-white text-orange-600 rounded-full font-semibold hover:bg-gray-50 transform hover:scale-105 transition-all duration-200 shadow-lg">
            Make a Donation
          </button>
          <button @click="showGallery" 
            class="px-8 py-4 border-2 border-white text-white rounded-full font-semibold hover:bg-white hover:text-orange-600 transform hover:scale-105 transition-all duration-200">
            View Our Work
          </button>
        </div>
      </div>
    </section>
  </div>
</template>