<script setup>
import { ref } from 'vue'

// Props to receive navigation functions from parent
const props = defineProps({
  showMission: Function,
  showDonate: Function,
  showGallery: Function
})

// Donation dialog state
const showDonationDialog = ref(true)
const closeDonationDialog = () => {
  showDonationDialog.value = false
}

// Direct PayPal donation function
const openPayPalDonation = () => {
  window.open('https://www.paypal.com/donate?hosted_button_id=48WGPF2XM7SNG', '_blank')
}
</script>

<template>
  <div class="home relative">
    <!-- Immediate Help Donation Dialog -->
    <div v-if="showDonationDialog" class="fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
      <div class="bg-white rounded-2xl max-w-lg w-full p-8 relative shadow-2xl border-4 border-yellow-600">
        <button @click="closeDonationDialog" class="absolute top-4 right-4 text-gray-500 hover:text-gray-800 text-2xl">
          ×
        </button>
        
        <div class="text-center">
          <div class="w-20 h-20 bg-gradient-to-br from-yellow-600 to-orange-600 rounded-full mx-auto mb-4 flex items-center justify-center">
            <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
            </svg>
          </div>
          
          <h3 class="text-2xl font-bold text-gray-800 mb-3">ছোট্ট হাতের বড় স্বপ্ন</h3>
          <h4 class="text-lg font-semibold text-yellow-700 mb-4">Little Hands, Big Dreams</h4>
          
          <p class="text-gray-700 mb-6 leading-relaxed">
            Right now, children in rural Bengal are waiting for books, uniforms, and a chance at education. 
            Your immediate support can change a life today.
          </p>
          
          <div class="bg-red-50 border-l-4 border-red-500 p-4 mb-6 text-left">
            <p class="text-red-800 font-semibold">Urgent Need:</p>
            <p class="text-red-700">50 children need school supplies this month</p>
            <p class="text-red-700">₹500 can educate one child for a month</p>
          </div>
          
          <div class="space-y-3">
            <button @click="openPayPalDonation" 
              class="w-full py-4 bg-gradient-to-r from-yellow-600 to-orange-600 text-white rounded-lg font-semibold hover:from-yellow-700 hover:to-orange-700 transition-all transform hover:scale-105 shadow-lg">
              Donate Now - Help Today
            </button>
            <button @click="closeDonationDialog" 
              class="w-full py-3 border-2 border-yellow-600 text-yellow-700 rounded-lg font-semibold hover:bg-yellow-50 transition-colors">
              Learn More First
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Hero Section with Bengali Aesthetic -->
    <section class="relative bg-gradient-to-br from-yellow-600 via-orange-600 to-red-600 text-white py-24 overflow-hidden">
      <!-- Traditional Bengali Pattern Overlay -->
      <div class="absolute inset-0 opacity-10">
        <div class="w-full h-full" style="background-image: url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2260%22 height=%2260%22 viewBox=%220 0 60 60%22><g fill=%22%23fff%22><circle cx=%2230%22 cy=%2230%22 r=%222%22/><circle cx=%2210%22 cy=%2210%22 r=%221%22/><circle cx=%2250%22 cy=%2210%22 r=%221%22/><circle cx=%2210%22 cy=%2250%22 r=%221%22/><circle cx=%2250%22 cy=%2250%22 r=%221%22/></g></svg>'); background-size: 60px 60px;"></div>
      </div>
      
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div class="text-center lg:text-left">
            <!-- Bengali Title -->
            <div class="mb-6">
              <h1 class="text-6xl lg:text-7xl font-bold mb-4 text-yellow-100" style="font-family: 'Noto Sans Bengali', serif;">
                বিদ্যাঙ্গদেহী
              </h1>
              <h2 class="text-4xl lg:text-5xl font-bold leading-tight">
                Educating
                <span class="block text-yellow-200">Young Minds</span>
                <span class="block text-orange-200">of Bengal</span>
              </h2>
            </div>
            
            <p class="text-xl mb-8 text-orange-100 leading-relaxed">
              শিক্ষার আলোয় আলোকিত করি বাংলার প্রতিটি ঘর<br>
              <em>Illuminating every home in Bengal with the light of education</em>
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
              <button @click="openPayPalDonation" 
                class="px-10 py-5 bg-white text-red-600 rounded-full font-bold hover:bg-yellow-50 transform hover:scale-105 transition-all duration-200 shadow-2xl border-2 border-yellow-300">
                🤝 আজই সাহায্য করুন
              </button>
              <button @click="showMission" 
                class="px-8 py-4 border-3 border-white text-white rounded-full font-semibold hover:bg-white hover:text-red-600 transform hover:scale-105 transition-all duration-200">
                আমাদের লক্ষ্য
              </button>
            </div>
          </div>
          
          <!-- Bengali Cultural Element -->
          <div class="relative">
            <div class="w-80 h-80 mx-auto relative">
              <!-- Traditional Bengali Alpona Pattern -->
              <div class="absolute inset-0 bg-white bg-opacity-20 rounded-full border-4 border-yellow-300 border-dashed animate-pulse"></div>
              <div class="w-full h-full bg-gradient-to-br from-yellow-400 to-orange-500 rounded-full flex items-center justify-center shadow-2xl border-4 border-white">
                <!-- Traditional Lamp/Diya Icon -->
                <div class="text-center">
                  <svg class="w-24 h-24 text-white mb-4 mx-auto" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.94-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/>
                  </svg>
                  <div class="text-white font-bold text-lg" style="font-family: 'Noto Sans Bengali', serif;">
                    জ্ঞানের আলো
                  </div>
                  <div class="text-white opacity-90 text-sm">Light of Knowledge</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Impact Stats with Bengali Touch -->
    <section class="py-16 bg-gradient-to-r from-yellow-50 to-orange-50 border-t-4 border-yellow-600">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold text-gray-800 mb-2" style="font-family: 'Noto Sans Bengali', serif;">আমাদের প্রভাব</h2>
          <p class="text-lg text-gray-600">Our Impact in Numbers</p>
        </div>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
          <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-yellow-600 text-center hover:shadow-xl transition-shadow">
            <div class="text-4xl font-bold text-yellow-700 mb-2">১০০০+</div>
            <div class="text-gray-700 font-semibold">ছাত্রছাত্রী</div>
            <div class="text-sm text-gray-500">Students Educated</div>
          </div>
          <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-orange-600 text-center hover:shadow-xl transition-shadow">
            <div class="text-4xl font-bold text-orange-700 mb-2">৫০+</div>
            <div class="text-gray-700 font-semibold">গ্রাম</div>
            <div class="text-sm text-gray-500">Villages Reached</div>
          </div>
          <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-red-600 text-center hover:shadow-xl transition-shadow">
            <div class="text-4xl font-bold text-red-700 mb-2">২৫+</div>
            <div class="text-gray-700 font-semibold">ত্রাণ কর্মসূচি</div>
            <div class="text-sm text-gray-500">Relief Programs</div>
          </div>
          <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-green-600 text-center hover:shadow-xl transition-shadow">
            <div class="text-4xl font-bold text-green-700 mb-2">৫০০০+</div>
            <div class="text-gray-700 font-semibold">জীবন পরিবর্তন</div>
            <div class="text-sm text-gray-500">Lives Transformed</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Story Section with Real Impact -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-800 mb-4" style="font-family: 'Noto Sans Bengali', serif;">
            সত্যি গল্প
          </h2>
          <h3 class="text-2xl font-semibold text-yellow-700 mb-4">Real Stories of Change</h3>
          <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            Every donation creates a story. Here are some lives changed through education and support.
          </p>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <!-- Story Card 1 -->
          <div class="bg-gradient-to-br from-yellow-50 to-orange-50 rounded-2xl p-8 shadow-lg border-2 border-yellow-200 hover:shadow-xl transition-all">
            <div class="text-center mb-6">
              <div class="w-20 h-20 bg-gradient-to-br from-yellow-600 to-orange-600 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span class="text-2xl text-white font-bold">রিয়া</span>
              </div>
              <h3 class="text-xl font-bold text-gray-800">Riya's Dream</h3>
              <p class="text-yellow-700 font-semibold">Age 12, Murshidabad</p>
            </div>
            <p class="text-gray-700 mb-6 leading-relaxed">
              "আমার স্বপ্ন ডাক্তার হওয়ার। বিদ্যাঙ্গদেহীর সাহায্যে এখন আমি স্কুলে যেতে পারি।"
            </p>
            <p class="text-sm text-gray-600 italic">
              "My dream is to become a doctor. With Bidyangdehi's help, I can now go to school."
            </p>
            <div class="mt-4 p-3 bg-white rounded-lg border border-yellow-300">
              <p class="text-sm text-gray-700"><strong>Impact:</strong> School fees, books, and uniform provided</p>
            </div>
          </div>

          <!-- Story Card 2 -->
          <div class="bg-gradient-to-br from-orange-50 to-red-50 rounded-2xl p-8 shadow-lg border-2 border-orange-200 hover:shadow-xl transition-all">
            <div class="text-center mb-6">
              <div class="w-20 h-20 bg-gradient-to-br from-orange-600 to-red-600 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span class="text-2xl text-white font-bold">অমিত</span>
              </div>
              <h3 class="text-xl font-bold text-gray-800">Amit's Success</h3>
              <p class="text-orange-700 font-semibold">Age 16, Nadia</p>
            </div>
            <p class="text-gray-700 mb-6 leading-relaxed">
              "কোভিডের সময় আমাদের পরিবারের খুব কষ্ট হয়েছিল। বিদ্যাঙ্গদেহী আমাদের পাশে দাঁড়িয়েছে।"
            </p>
            <p class="text-sm text-gray-600 italic">
              "During COVID, our family faced great hardship. Bidyangdehi stood by us."
            </p>
            <div class="mt-4 p-3 bg-white rounded-lg border border-orange-300">
              <p class="text-sm text-gray-700"><strong>Support:</strong> Emergency food and medical aid</p>
            </div>
          </div>

          <!-- Urgent Need Card -->
          <div class="bg-gradient-to-br from-red-50 to-pink-50 rounded-2xl p-8 shadow-lg border-2 border-red-300 hover:shadow-xl transition-all">
            <div class="text-center mb-6">
              <div class="w-20 h-20 bg-gradient-to-br from-red-600 to-pink-600 rounded-full mx-auto mb-4 flex items-center justify-center">
                <svg class="w-10 h-10 text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
              <h3 class="text-xl font-bold text-gray-800">আজই সাহায্য প্রয়োজন</h3>
              <p class="text-red-700 font-semibold">Immediate Help Needed</p>
            </div>
            <p class="text-gray-700 mb-6 leading-relaxed">
              50 children are waiting for school supplies this month. Your support can change their future.
            </p>
            <div class="space-y-3">
              <div class="p-3 bg-white rounded-lg border border-red-300">
                <p class="text-sm text-gray-700"><strong>₹500</strong> - One month education</p>
              </div>
              <button @click="openPayPalDonation" 
                class="w-full py-3 bg-gradient-to-r from-red-600 to-pink-600 text-white rounded-lg font-semibold hover:from-red-700 hover:to-pink-700 transition-all">
                Help Now
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Quote Section -->
    <section class="py-20 bg-gradient-to-r from-gray-800 to-gray-900 text-white relative overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="w-full h-full" style="background-image: url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2240%22 height=%2240%22 viewBox=%220 0 40 40%22><g fill=%22%23fff%22><path d=%22M20 20c0-5.5-4.5-10-10-10s-10 4.5-10 10 4.5 10 10 10 10-4.5 10-10zm10 0c0-5.5-4.5-10-10-10s-10 4.5-10 10 4.5 10 10 10 10-4.5 10-10z%22/></g></svg>'); background-size: 40px 40px;"></div>
      </div>
      <div class="relative max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <div class="mb-8">
          <div class="text-6xl mb-4" style="font-family: 'Noto Sans Bengali', serif; color: #fbbf24;">
            "শিক্ষাই জাতির মেরুদণ্ড"
          </div>
        </div>
        <blockquote class="text-3xl lg:text-4xl font-light italic mb-8 leading-relaxed text-yellow-200">
          "Education is the manifestation of the perfection already in man"
        </blockquote>
        <cite class="text-xl text-gray-300">— Swami Vivekananda</cite>
      </div>
    </section>

    <!-- Final CTA Section -->
    <section class="py-20 bg-gradient-to-br from-yellow-600 via-orange-600 to-red-600 text-white">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-5xl font-bold mb-4" style="font-family: 'Noto Sans Bengali', serif;">
          আজই যোগ দিন
        </h2>
        <h3 class="text-3xl font-bold mb-6">Join Our Mission Today</h3>
        <p class="text-xl mb-8 opacity-90 leading-relaxed">
          আপনার সামান্য অনুদান একটি শিশুর ভবিষ্যৎ পরিবর্তন করতে পারে।<br>
          <em>Your small donation can change a child's future forever.</em>
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm">
            <div class="text-2xl font-bold mb-2">₹500</div>
            <div class="text-sm">One month education</div>
          </div>
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm">
            <div class="text-2xl font-bold mb-2">₹2000</div>
            <div class="text-sm">School supplies for 5 children</div>
          </div>
          <div class="bg-white bg-opacity-20 rounded-lg p-4 backdrop-blur-sm">
            <div class="text-2xl font-bold mb-2">₹5000</div>
            <div class="text-sm">Emergency relief for a family</div>
          </div>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button @click="openPayPalDonation" 
            class="px-12 py-5 bg-white text-red-600 rounded-full font-bold hover:bg-yellow-50 transform hover:scale-105 transition-all duration-200 shadow-2xl border-4 border-yellow-300 text-lg">
            🤝 দান করুন - Donate Now
          </button>
          <button @click="showGallery" 
            class="px-8 py-4 border-3 border-white text-white rounded-full font-semibold hover:bg-white hover:text-red-600 transform hover:scale-105 transition-all duration-200">
            আমাদের কাজ দেখুন - View Our Work
          </button>
        </div>
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