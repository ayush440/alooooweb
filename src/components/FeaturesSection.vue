<template>
  <section class="w-full bg-white py-20 font-inter">
    <div class="max-w-[1800px] mx-auto px-[43px]">
      <!-- Main Heading -->
      <h2 class="text-[48px] text-[#2F5741] font-bold text-center mb-20">
        Designed for beginners and experienced traders
      </h2>

      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
        <!-- Trading Platform Card -->
        <div class="bg-white rounded-lg p-10 text-center border border-gray-100 shadow-sm hover:shadow-md transition-shadow duration-300">
          <div class="flex justify-center mb-8">
            <img 
              src="../assets/images/Gainers.svg"
              alt="Trading Platform" 
              class="w-20 h-20"
            />
          </div>
          <h3 class="text-[#2F5741] text-2xl font-semibold mb-5">
            Trading Platform
          </h3>
          <p class="text-[#666666] text-lg leading-relaxed">
            We offer low fees and fast execution times, so you can make the most of it.
          </p>
        </div>

        <!-- 24/7 Support Card -->
        <div class="bg-white rounded-lg p-10 text-center border border-gray-100 shadow-sm hover:shadow-md transition-shadow duration-300">
          <div class="flex justify-center mb-8">
            <img 
              src="../assets/images/Support.svg"
              alt="24/7 Support" 
              class="w-20 h-20"
            />
          </div>
          <h3 class="text-[#2F5741] text-2xl font-semibold mb-5">
            24/7 Support
          </h3>
          <p class="text-[#666666] text-lg leading-relaxed">
            Get round-the-clock assistance from our expert team for any queries.
          </p>
        </div>

        <!-- Effortless Trading Card -->
        <div class="bg-white rounded-lg p-10 text-center border border-gray-100 shadow-sm hover:shadow-md transition-shadow duration-300">
          <div class="flex justify-center mb-8">
            <img 
              src="../assets/images/Cloud.svg"
              alt="Effortless Trading" 
              class="w-20 h-20"
            />
          </div>
          <h3 class="text-[#2F5741] text-2xl font-semibold mb-5">
            Effortless Trading, Anytime
          </h3>
          <p class="text-[#666666] text-lg leading-relaxed">
            Get real-time notifications for every trade you perform.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script setup required for this component
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

.font-inter {
  font-family: 'Inter', sans-serif;
}

.hover\:shadow-md {
  transition: box-shadow 0.3s ease-in-out;
}
</style>