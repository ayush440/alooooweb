<template>
  <div class="min-h-screen flex flex-col">
    <HeroSection />
    <FeaturesSection />
    <BenefitsSection />
    <BlendSection />
    <PricingSection />
    <GettingStartedSection />
    <CommunitySection />
    <FooterSection />
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import BenefitsSection from './components/BenefitsSection.vue'
import BlendSection from './components/BlendSection.vue'
import PricingSection from './components/PricingSection.vue'
import GettingStartedSection from './components/GettingStartedSection.vue'
import CommunitySection from './components/CommunitySection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

@tailwind base;
@tailwind components;
@tailwind utilities;

:root {
  font-family: 'Inter', sans-serif;
}

html, body {
  @apply m-0 p-0 overflow-x-hidden;
  width: 100%;
}

body {
  @apply antialiased leading-normal;
}

h1, h2, h3, h4, h5, h6 {
  @apply leading-tight;
}

button {
  @apply cursor-pointer border-none outline-none;
}

img {
  @apply max-w-full h-auto;
}

a {
  @apply no-underline text-inherit;
}
</style>