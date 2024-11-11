<template>
    <section class="w-full py-20">
      <div class="max-w-[1271px] mx-auto px-6">
        <!-- Heading Section -->
        <div class="text-center mb-[60px]">
          <h2 class="text-[40px] font-bold mb-6">
            <span class="text-[#2F5741]">How to </span>
            <span class="text-[#FFB800]">get Started</span>
          </h2>
          <p class="text-[#666666] text-lg max-w-[900px] mx-auto leading-[27px]">
            Our pricing plans are designed to suit traders of all levels, offering flexible options without hidden fees. Get access to premium features and expert tools that help you maximize your returns while minimizing costs.
          </p>
        </div>
  
        <!-- Steps Section -->
        <div class="flex flex-wrap justify-between items-start gap-8">
          <div v-for="(step, index) in steps" :key="index" class="flex-1 min-w-[200px]">
            <div class="flex flex-col items-center text-center">
              <div class="w-[96px] h-[96px] bg-[#F8F8F8] rounded-full flex items-center justify-center mb-6">
                <component :is="step.icon" class="w-12 h-12 text-[#2F5741]" />
              </div>
              <h3 class="text-[#2F5741] text-[20px] font-semibold mb-3">{{ step.title }}</h3>
              <p class="text-[#666666] text-[16px] leading-[24px] max-w-[200px]">{{ step.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { UserCircle, Wallet, Handshake, LineChart, ArrowRight } from 'lucide-vue-next'
  
  const steps = [
    {
      title: "Get started",
      description: "Initiate by signing up or logging in your account",
      icon: UserCircle
    },
    {
      title: "Select a plan",
      description: "Pick the right subscription plan for yourself",
      icon: Wallet
    },
    {
      title: "Add a broker",
      description: "Add a suitable broker to your account or open a demat account",
      icon: Handshake
    },
    {
      title: "Select strategy",
      description: "Choose a strategy that fits your investment size and risk tolerance.",
      icon: LineChart
    },
    {
      title: "Start trading",
      description: "Ready set start trading with a click of a button",
      icon: ArrowRight
    }
  ]
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
  
  :root {
    font-family: 'Inter', sans-serif;
  }
  </style>