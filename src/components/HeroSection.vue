<template>
  <div class="w-full bg-[#FFFBE9]">
    <!-- Navigation Bar -->
    <nav class="py-4 pl-[70px] pr-4 sm:pr-8 lg:pr-16">
      <div class="max-w-[1800px] mx-auto flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center">
          <img 
            src="../assets/images/Algo.svg" 
            alt="Algorrithm Logo" 
            class="h-12 w-auto"
          />
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden lg:flex items-center">
          <div class="bg-white rounded-[50px] px-8 py-3 flex items-center">
            <div class="flex items-center gap-12 mr-6">
              <a 
                v-for="link in navLinks" 
                :key="link" 
                href="#" 
                class="text-[#4A4A4A] hover:text-[#2F5741] text-base font-medium transition-colors duration-200"
              >
                {{ link }}
              </a>
            </div>
            <button class="bg-[#2F5741] text-white px-8 py-2 rounded-full text-base font-medium hover:bg-opacity-90 transition-all duration-200">
              Login /Signup
            </button>
          </div>
        </div>

        <!-- Mobile Menu Button -->
        <button 
          @click="toggleMenu"
          class="lg:hidden flex flex-col justify-center items-center w-10 h-10 space-y-1.5 focus:outline-none"
          aria-label="Toggle menu"
        >
          <span 
            class="w-8 h-0.5 bg-[#2F5741] transition-all duration-300"
            :class="{ 'rotate-45 translate-y-2': isMenuOpen }"
          ></span>
          <span 
            class="w-8 h-0.5 bg-[#2F5741] transition-all duration-300"
            :class="{ 'opacity-0': isMenuOpen }"
          ></span>
          <span 
            class="w-8 h-0.5 bg-[#2F5741] transition-all duration-300"
            :class="{ '-rotate-45 -translate-y-2': isMenuOpen }"
          ></span>
        </button>
      </div>

      <!-- Mobile Navigation -->
      <div 
        class="lg:hidden overflow-hidden transition-all duration-300 ease-in-out"
        :class="isMenuOpen ? 'max-h-96' : 'max-h-0'"
      >
        <div class="bg-white shadow-lg mt-4 rounded-3xl px-6 py-8 space-y-6">
          <a 
            v-for="link in navLinks" 
            :key="link" 
            href="#" 
            class="block text-[#4A4A4A] hover:text-[#2F5741] text-lg font-medium transition-colors duration-200"
          >
            {{ link }}
          </a>
          <button class="bg-[#2F5741] text-white px-6 py-2 rounded-full text-base font-medium hover:bg-opacity-90 transition-all duration-200 w-full">
            Login /Signup
          </button>
        </div>
      </div>
    </nav>

    <!-- Hero Content -->
    <div class="max-w-[1800px] mx-auto pl-[70px] pr-4 sm:pr-8 lg:pr-16 pb-24 pt-16 relative">
      <div class="flex flex-col lg:flex-row items-start justify-between">
        <div class="w-full lg:w-[45%] flex flex-col items-start">
          <h1 class="text-[64px] leading-[1.1] font-bold mb-8 mt-24">
            <span class="text-[#2D2D2D] inline-block">Super</span>
            <span class="text-[#2F5741] ml-2 ">Algo Trading Platform</span>
          
            <span class="text-[#2D2D2D] ml-2 ">for super</span>
            <br />
            <span class="text-[#2D2D2D] ">traders</span>
          </h1>
          
          <p class="text-[#666666] text-xl leading-relaxed mb-12 max-w-[620px]">
            Our algorithmic trading software automates complex strategies, delivering speed and precision in every trade. Maximize profits, reduce risks, and stay ahead of the market with seamless, data-driven execution.
          </p>

          <button class="bg-[#2F5741] text-white px-10 py-4 rounded-full text-xl font-medium hover:bg-opacity-90 transition-all duration-300">
            Get Started
          </button>
        </div>
        <div class="w-full lg:w-[55%] flex items-center justify-end mt-12 lg:mt-0 relative lg:absolute lg:bottom-0 lg:right-0 overflow-hidden">
          <img 
            src="../assets/images/image2.png"
            alt="Trading Platform Interface" 
            class="w-full h-auto object-contain lg:object-bottom"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const navLinks = ['Why Algo', 'Features', 'Pricing', 'About Us', 'Why Us']
const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

:root {
  font-family: 'Inter', sans-serif;
}

html {
  scroll-behavior: smooth;
}
</style>