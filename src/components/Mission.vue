<script setup>
import { ref } from 'vue'

// Props to receive navigation functions from parent
const props = defineProps({
  showHome: Function,
  showBeneficiaries: Function
})

// Direct PayPal donation function
const openPayPalDonation = () => {
  window.open('https://www.paypal.com/donate?hosted_button_id=48WGPF2XM7SNG', '_blank')
}
</script>

<template>
  <div class="mission">
    <!-- Hero Section with Bengali Aesthetic -->
    <section class="bg-gradient-to-br from-yellow-600 via-orange-600 to-red-600 text-white py-24 overflow-hidden relative">
      <!-- Traditional Bengali Pattern Overlay -->
      <div class="absolute inset-0 opacity-10">
        <div class="w-full h-full" style="background-image: url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2260%22 height=%2260%22 viewBox=%220 0 60 60%22><g fill=%22%23fff%22><circle cx=%2230%22 cy=%2230%22 r=%222%22/><circle cx=%2210%22 cy=%2210%22 r=%221%22/><circle cx=%2250%22 cy=%2210%22 r=%221%22/><circle cx=%2210%22 cy=%2250%22 r=%221%22/><circle cx=%2250%22 cy=%2250%22 r=%221%22/></g></svg>'); background-size: 60px 60px;"></div>
      </div>
      
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-6xl font-bold mb-6 text-white">Our Mission</h1>
          <p class="text-xl max-w-4xl mx-auto opacity-90 leading-relaxed">
            Empowering Bengal's future through quality education, community development, and humanitarian relief programs that transform lives and strengthen communities.
          </p>
          <p class="text-lg text-yellow-200 mt-4 italic" style="font-family: 'Noto Sans Bengali', serif;">
            "শিক্ষাই জাতির মেরুদণ্ড" - Education is the backbone of the nation
          </p>
        </div>
      </div>
    </section>

    <!-- Core Mission with Bengali Touch -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div>
            <h2 class="text-4xl font-bold text-gray-800 mb-6">Transforming Lives Through Education</h2>
            
            <p class="text-lg text-gray-700 mb-6 leading-relaxed">
              Bidyangdehi is committed to providing quality education to underprivileged children across Bengal. 
              We believe that education is the most powerful tool to break the cycle of poverty and create 
              sustainable change in communities.
            </p>
            
            <p class="text-lg text-gray-600 mb-8 leading-relaxed">
              Our programs focus on holistic development, combining academic excellence with character building, 
              practical skills, and cultural values rooted in Bengali traditions. We work directly with families 
              and communities to ensure lasting impact.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4">
              <button @click="showBeneficiaries" 
                class="px-8 py-4 bg-gradient-to-r from-yellow-600 to-orange-600 text-white rounded-lg hover:from-yellow-700 hover:to-orange-700 transition-all font-semibold shadow-lg transform hover:scale-105">
                Meet Our Beneficiaries
              </button>
              <button @click="openPayPalDonation" 
                class="px-8 py-4 border-2 border-yellow-600 text-yellow-700 rounded-lg hover:bg-yellow-50 transition-all font-semibold">
                🤝 Help Today
              </button>
            </div>
          </div>
          
          <div class="relative">
            <div class="bg-gradient-to-br from-yellow-400 to-orange-500 rounded-2xl p-8 shadow-2xl border-4 border-yellow-300">
              <div class="text-center text-white">
                <svg class="w-28 h-28 mx-auto mb-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
                <h3 class="text-3xl font-bold mb-3" style="font-family: 'Noto Sans Bengali', serif;">বিদ্যা দেহি</h3>
                <p class="text-xl opacity-90 mb-2">Grant us Knowledge</p>
                <p class="text-sm opacity-80" style="font-family: 'Noto Sans Bengali', serif;">
                  "সর্বজনের হিতে যার কাজ, তারই জীবন সার্থক আজ"
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Vision & Values with Bengali Design -->
    <section class="py-20 bg-gradient-to-r from-yellow-50 to-orange-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-800 mb-4">Our Vision & Values</h2>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Building a society where every child has access to quality education and opportunities to thrive.
          </p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- Vision Card -->
          <div class="bg-white rounded-xl shadow-lg p-8 text-center hover:shadow-xl transition-shadow border-2 border-yellow-200">
            <div class="w-20 h-20 bg-gradient-to-br from-yellow-500 to-orange-600 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 4.5C7 4.5 2.73 7.61 1 12c1.73 4.39 6 7.5 11 7.5s9.27-3.11 11-7.5c-1.73-4.39-6-7.5-11-7.5zM12 17c-2.76 0-5-2.24-5-5s2.24-5 5-5 5 2.24 5 5-2.24 5-5 5zm0-8c-1.66 0-3 1.34-3 3s1.34 3 3 3 3-1.34 3-3-1.34-3-3-3z"/>
              </svg>
            </div>
            <h3 class="text-xl font-bold text-gray-800 mb-4">Our Vision</h3>
            <p class="text-gray-600 leading-relaxed">
              A world where education empowers every individual to reach their full potential and contribute meaningfully to society.
            </p>
          </div>

          <!-- Mission Card -->
          <div class="bg-white rounded-xl shadow-lg p-8 text-center hover:shadow-xl transition-shadow border-2 border-orange-200">
            <div class="w-20 h-20 bg-gradient-to-br from-orange-500 to-red-600 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <h3 class="text-xl font-bold text-gray-800 mb-4">Our Mission</h3>
            <p class="text-gray-600 leading-relaxed">
              To provide accessible, quality education and support services that transform lives and strengthen communities across Bengal.
            </p>
          </div>

          <!-- Values Card -->
          <div class="bg-white rounded-xl shadow-lg p-8 text-center hover:shadow-xl transition-shadow border-2 border-red-200">
            <div class="w-20 h-20 bg-gradient-to-br from-red-500 to-pink-600 rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
              </svg>
            </div>
            <h3 class="text-xl font-bold text-gray-800 mb-4">Our Values</h3>
            <p class="text-gray-600 leading-relaxed">
              Compassion, integrity, excellence, and cultural respect guide everything we do in service of our communities.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Programs Overview with Bengali Style -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-800 mb-4">Our Programs</h2>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Comprehensive initiatives designed to address education, health, and emergency relief needs across Bengal.
          </p>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
          <!-- Education Programs -->
          <div class="bg-gradient-to-br from-yellow-50 to-orange-50 rounded-2xl p-8 border-2 border-yellow-200">
            <h3 class="text-2xl font-bold text-gray-800 mb-6">Educational Initiatives</h3>
            
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-yellow-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-yellow-400">
                  <svg class="w-7 h-7 text-yellow-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 3L1 9l4 2.18v6L12 21l7-3.82v-6l2-1.09V17h2V9L12 3zm6.82 6L12 12.72 5.18 9 12 5.28 18.82 9zM17 15.99l-5 2.73-5-2.73v-3.72L12 15l5-2.73v3.72z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">Primary Education Support</h5>
                  <p class="text-gray-600 leading-relaxed">Providing books, uniforms, and educational materials to children in rural Bengal schools.</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-green-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-green-400">
                  <svg class="w-7 h-7 text-green-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M19.14,12.94c0.04-0.3,0.06-0.61,0.06-0.94c0-0.32-0.02-0.64-0.07-0.94l2.03-1.58c0.18-0.14,0.23-0.41,0.12-0.61 l-1.92-3.32c-0.12-0.22-0.37-0.29-0.59-0.22l-2.39,0.96c-0.5-0.38-1.03-0.7-1.62-0.94L14.4,2.81c-0.04-0.24-0.24-0.41-0.48-0.41 h-3.84c-0.24,0-0.43,0.17-0.47,0.41L9.25,5.35C8.66,5.59,8.12,5.92,7.63,6.29L5.24,5.33c-0.22-0.08-0.47,0-0.59,0.22L2.74,8.87 C2.62,9.08,2.66,9.34,2.86,9.48l2.03,1.58C4.84,11.36,4.82,11.69,4.82,12s0.02,0.64,0.07,0.94l-2.03,1.58 c-0.18,0.14-0.23,0.41-0.12,0.61l1.92,3.32c0.12,0.22,0.37,0.29,0.59,0.22l2.39-0.96c0.5,0.38,1.03,0.7,1.62,0.94l0.36,2.54 c0.05,0.24,0.24,0.41,0.48,0.41h3.84c0.24,0,0.44-0.17,0.47-0.41l0.36-2.54c0.59-0.24,1.13-0.56,1.62-0.94l2.39,0.96 c0.22,0.08,0.47,0,0.59-0.22l1.92-3.32c0.12-0.22,0.07-0.47-0.12-0.61L19.14,12.94z M12,15.6c-1.98,0-3.6-1.62-3.6-3.6 s1.62-3.6,3.6-3.6s3.6,1.62,3.6,3.6S13.98,15.6,12,15.6z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">Skill Development</h5>
                  <p class="text-gray-600 leading-relaxed">Vocational training programs to equip youth with practical skills for employment opportunities.</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-purple-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-purple-400">
                  <svg class="w-7 h-7 text-purple-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M9.4 16.6L4.8 12l4.6-4.6L8 6l-6 6 6 6 1.4-1.4zm5.2 0L19.2 12l-4.6-4.6L16 6l6 6-6 6-1.4-1.4z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">Digital Literacy</h5>
                  <p class="text-gray-600 leading-relaxed">Computer and internet literacy programs to bridge the digital divide in rural communities.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Relief Programs -->
          <div class="bg-gradient-to-br from-orange-50 to-red-50 rounded-2xl p-8 border-2 border-orange-200">
            <h3 class="text-2xl font-bold text-gray-800 mb-6">Relief & Support</h3>
            
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-red-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-red-400">
                  <svg class="w-7 h-7 text-red-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">COVID-19 Relief</h5>
                  <p class="text-gray-600 leading-relaxed">Emergency support including food, medical supplies, and financial assistance during the pandemic.</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-yellow-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-yellow-400">
                  <svg class="w-7 h-7 text-yellow-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2L13.09 8.26L22 9L17.5 14.74L22 22L12 17L2 22L6.5 14.74L2 9L10.91 8.26L12 2Z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">Disaster Relief</h5>
                  <p class="text-gray-600 leading-relaxed">Rapid response support for communities affected by natural disasters like Cyclone Amphan.</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="w-14 h-14 bg-teal-200 rounded-lg flex items-center justify-center flex-shrink-0 border-2 border-teal-400">
                  <svg class="w-7 h-7 text-teal-700" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
                  </svg>
                </div>
                <div>
                  <h5 class="text-lg font-semibold text-gray-800 mb-2">Healthcare Support</h5>
                  <p class="text-gray-600 leading-relaxed">Medical camps, health awareness programs, and access to essential healthcare services.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action with Bengali Style -->
    <section class="py-20 bg-gradient-to-br from-yellow-600 via-orange-600 to-red-600 text-white relative overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="w-full h-full" style="background-image: url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2240%22 height=%2240%22 viewBox=%220 0 40 40%22><g fill=%22%23fff%22><path d=%22M20 20c0-5.5-4.5-10-10-10s-10 4.5-10 10 4.5 10 10 10 10-4.5 10-10zm10 0c0-5.5-4.5-10-10-10s-10 4.5-10 10 4.5 10 10 10 10-4.5 10-10z%22/></g></svg>'); background-size: 40px 40px;"></div>
      </div>
      <div class="relative max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-5xl font-bold mb-6">Join Our Mission</h2>
        <p class="text-xl mb-8 opacity-90 leading-relaxed">
          Together, we can create lasting change in the lives of children and communities across Bengal. 
          Your support helps provide education, relief, and hope to those who need it most.
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm border border-yellow-300">
            <div class="text-2xl font-bold mb-2">₹500</div>
            <div class="text-sm">One month education</div>
            <div class="text-xs opacity-80">Books, supplies & support</div>
          </div>
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm border border-yellow-300">
            <div class="text-2xl font-bold mb-2">₹2000</div>
            <div class="text-sm">School supplies for 5 children</div>
            <div class="text-xs opacity-80">Complete educational kit</div>
          </div>
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm border border-yellow-300">
            <div class="text-2xl font-bold mb-2">₹5000</div>
            <div class="text-sm">Emergency relief for a family</div>
            <div class="text-xs opacity-80">Food, medical & essentials</div>
          </div>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button @click="openPayPalDonation" 
            class="px-12 py-5 bg-white text-red-600 rounded-full font-bold hover:bg-yellow-50 transform hover:scale-105 transition-all duration-200 shadow-2xl border-4 border-yellow-300 text-lg">
            🤝 Donate Now
          </button>
          <button @click="showBeneficiaries" 
            class="px-8 py-4 border-3 border-white text-white rounded-full font-semibold hover:bg-white hover:text-red-600 transform hover:scale-105 transition-all duration-200">
            See Our Impact
          </button>
          <button @click="showHome" 
            class="px-8 py-4 border-2 border-white text-white rounded-full font-semibold hover:bg-white hover:text-red-600 transform hover:scale-105 transition-all duration-200">
            Back to Home
          </button>
        </div>
        
        <p class="text-sm text-yellow-200 mt-6 italic" style="font-family: 'Noto Sans Bengali', serif;">
          "দানে মেলে পুণ্য, সেবায় মেলে জীবন" - Virtue comes from giving, life comes from service
        </p>
      </div>
    </section>
  </div>
</template>

<style scoped>
/* Import Bengali font */
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&display=swap');

/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

/* Bengali text styling */
.bengali-text {
  font-family: 'Noto Sans Bengali', serif;
}
</style>