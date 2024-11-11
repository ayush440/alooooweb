<template>
  <section 
    ref="sectionRef" 
    class="w-full py-32 relative overflow-hidden transition-colors duration-1000"
    :class="[isInView ? 'bg-[#3A6148]' : 'bg-white']"
  >
    <div class="max-w-[1440px] mx-auto px-6 h-96 ">
      <div class="relative z-10">
        <h2 
          ref="headingRef" 
          class="text-4xl md:text-5xl lg:text-7xl font-bold text-center leading-tight max-w-[1200px] mx-auto opacity-0"
        >
          <span 
            class="inline-block transition-colors duration-1000" 
            :class="[isInView ? 'text-white' : 'text-[#black]']"
          >
            Discover the perfect blend of
          </span>
          <br class="hidden md:block" />
          <span class="inline-block">
            <span 
              v-for="(word, index) in highlightedWords" 
              :key="index"
              class="inline-block transition-colors duration-1000 highlighted-word"
              :class="[isInView ? 'text-[#FFB800]' : 'text-white']"
            >
              {{ word }}
            </span>
          </span>
        </h2>
      </div>

      <!-- Abstract background shapes -->
      <div 
        class="absolute inset-0 opacity-10 transition-opacity duration-1000" 
        :class="{ 'opacity-0': !isInView }"
      >
        <div class="absolute top-0 left-0 w-64 h-64 rounded-full  blur-3xl transform -translate-x-1/2 -translate-y-1/2"></div>
        <div class="absolute bottom-0 right-0 w-64 h-64 rounded-full  blur-3xl transform translate-x-1/2 translate-y-1/2"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const sectionRef = ref(null)
const headingRef = ref(null)
const isInView = ref(false)
const hasAnimated = ref(false)

const highlightedWords = ['care,', 'reliability', 'and', 'usability']

onMounted(() => {
  if (sectionRef.value && headingRef.value) {
    ScrollTrigger.create({
      trigger: sectionRef.value,
      start: "top 80%",
      onEnter: () => {
        if (!hasAnimated.value) {
          isInView.value = true
          hasAnimated.value = true

          // Heading animation
          gsap.fromTo(headingRef.value, 
            { y: 100, opacity: 0 },
            { y: 0, opacity: 1, duration: 2.0, ease: 'power4.out' }
          )

          // Background color change
          gsap.to(sectionRef.value, {
            backgroundColor: '#3A6148',
            duration: 1.5,
            ease: 'power2.inOut',
          })

          // Text color change for "Discover the perfect blend of"
          gsap.to(headingRef.value.querySelector('span:first-child'), {
            color: 'white',
            duration: 1.5,
            ease: 'power2.inOut',
          })

          // Highlighted words color transition
          gsap.to('.highlighted-word', {
            color: '#FFB800',
            duration: 0.5,
            stagger: 0.2,
            ease: 'power2.inOut'
          })
        }
      },
      once: true
    })
  }
})

onUnmounted(() => {
  // Clean up ScrollTrigger
  ScrollTrigger.getAll().forEach(trigger => trigger.kill())
})
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

.highlighted-word {
  margin: 0 0.2em;
}

.transition-colors {
  transition-property: color, background-color;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>