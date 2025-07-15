<script setup>
// Props to receive navigation functions from parent
defineProps({
  showHome: Function,
  showBeneficiaries: Function
})
</script>

<template>
  <div class="mission">
    <!-- Hero Section -->
    <section class="bg-gradient-to-br from-blue-600 to-purple-700 text-white py-20">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center">
          <h1 class="text-5xl font-bold mb-6">Our Mission</h1>
          <p class="text-xl max-w-3xl mx-auto opacity-90">
            Empowering India's future through quality education, community development, and humanitarian relief programs.
          </p>
        </div>
      </div>
    </section>

    <!-- Core Mission -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div>
            <h2 class="text-4xl font-bold text-gray-800 mb-6">Transforming Lives Through Education</h2>
            <p class="text-lg text-gray-600 mb-6">
              Bidyangdehi is committed to providing quality education to underprivileged children across India. 
              We believe that education is the most powerful tool to break the cycle of poverty and create 
              sustainable change in communities.
            </p>
            <p class="text-lg text-gray-600 mb-8">
              Our programs focus on holistic development, combining academic excellence with character building, 
              practical skills, and cultural values rooted in Indian traditions.
            </p>
            <button @click="showBeneficiaries" 
              class="px-8 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors font-semibold">
              Meet Our Beneficiaries
            </button>
          </div>
          <div class="relative">
            <div class="bg-gradient-to-br from-yellow-400 to-orange-500 rounded-2xl p-8 shadow-2xl">
              <div class="text-center text-white">
                <svg class="w-24 h-24 mx-auto mb-4" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 3L1 9l4 2.18v6L12 21l7-3.82v-6l2-1.09V17h2V9L12 3zm6.82 6L12 12.72 5.18 9 12 5.28 18.82 9zM17 15.99l-5 2.73-5-2.73v-3.72L12 15l5-2.73v3.72z"/>
                </svg>
                <h3 class="text-2xl font-bold mb-2">विद्या देहि</h3>
                <p class="text-lg opacity-90">Grant us Knowledge</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Vision & Values -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold text-gray-