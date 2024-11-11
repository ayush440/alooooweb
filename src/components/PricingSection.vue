<template>
  <section class="w-full bg-[#3A6148] py-20">
    <div class="max-w-[1702px] mx-auto px-6 md:px-[69px]">
      <!-- Free Trial Box -->
      <div class="mb-8 w-full rounded-3xl relative overflow-visible h-[500px] md:h-[400px]">
        <div class="absolute inset-0 bg-white/10 backdrop-blur-md hover:bg-white/20 transition-all duration-300 rounded-3xl"></div>
        <div class="flex h-full relative">
          <!-- Text content -->
          <div class="w-full md:w-[45%] p-8 md:p-12 flex flex-col items-start justify-center z-10 md:ml-32">
            <h2 class="text-3xl md:text-5xl font-bold text-white mb-2 md:w-96">
              Free Trial for
              <br><span class="text-[#FFB800] inline-block mt-1">7 Days</span>
            </h2>
            <button class="bg-[#FFB800] text-white px-6 py-2 md:px-8 md:py-3 rounded-full mt-6 hover:bg-opacity-90 transition-all duration-300">
              Try Now
            </button>
          </div>
          <!-- Image container -->
          <div class="absolute right-[-5%] sm:right-[-10%] md:right-[-20%] lg:right-[-10%] top-[-60%] sm:top-[-50%] md:top-[-50%] lg:top-[-50%]  md:h-[150%]  h-[160%] w-[70%] hidden md:block overflow-visible">
            <img 
              src="../assets/images/image6.png"
              alt="Person using phone" 
              class="w-auto h-full object-cover object-center md:hidden lg:block"
            />
          </div>
        </div>
      </div>

      <!-- Two Column Layout -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-8">
        <!-- Daily Profit Box -->
        <div class="rounded-3xl overflow-hidden group relative h-[700px] md:h-[450px]">
          <div class="absolute inset-0 bg-white/10 backdrop-blur-md group-hover:bg-white/20 transition-all duration-300"></div>
          <div class="relative z-10 p-6 md:p-8 h-full flex flex-col items-center">
            <h3 class="text-xl md:text-4xl font-bold text-white text-center mt-10">
              Daily profit with perfect
              <br />
              <span class="text-[#FFB800]">Risk Management</span>
            </h3>
            <div class="relative flex-1 w-full mt-8 h-[300px]">
              <img 
                src="../assets/images/image.svg"
                alt="Trading Interface" 
                class="w-full h-full object-contain transform translate-x-52"
              />
            </div>
          </div>
        </div>

        <!-- X2 Box -->
        <div class="rounded-3xl overflow-hidden group relative h-[700px] md:h-[450px]">
          <div class="absolute inset-0 bg-white/10 backdrop-blur-md group-hover:bg-white/20 transition-all duration-300"></div>
          <div class="relative z-10 p-6 md:p-8 h-full flex flex-col items-center">
            <h3 class="text-xl md:text-4xl font-bold text-white text-center mt-10">
              Suitable for any type of
              <br />lot you decide
            </h3>
            <div class="relative flex-1 w-full mt-8 h-[300px]">
              <img 
                src="../assets/images/image8.svg"
                alt="X2 3D Logo" 
                class="w-full h-52 object-contain "
              />
            </div>
          </div>
        </div>
      </div>

      <!-- Clients Box -->
      <div class="mb-8 w-full rounded-3xl overflow-hidden group relative min-h-[240px]">
        <div class="absolute inset-0 bg-white/10 backdrop-blur-md group-hover:bg-white/20 transition-all duration-300"></div>
        <div class="relative z-10 p-6 md:p-12">
          <div class="flex flex-col md:flex-row justify-between items-center">
            <div class="flex flex-col justify-center md:ml-32 mb-6 md:mb-0">
              <h2 class="text-3xl md:text-5xl font-bold mb-1">
                <span class="text-[#FFB800]">500+</span>
                <span class="text-white ml-2">Client</span>
              </h2>
              <p class="text-xl md:text-2xl text-white mb-6">Across India</p>
              <button class="bg-[#FFB800] text-white px-8 py-3 rounded-full hover:bg-opacity-90 transition-all duration-300">
                Try Now
              </button>
            </div>
            <div class="w-full md:w-1/2 md:pr-12">
              <img 
                src="../assets/images/Untitled-1.svg"
                alt="Client Grid" 
                class="w-full h-auto object-contain md:hidden lg:block"
              />
            </div>
          </div>
        </div>
      </div>

      <!-- Bottom Two Column Layout -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Chart Box -->
        <div class="rounded-3xl overflow-hidden group relative h-[500px] md:h-[450px]">
          <div class="absolute inset-0 bg-white/10 backdrop-blur-md group-hover:bg-white/20 transition-all duration-300"></div>
          <div class="relative z-10 p-6 md:p-0 h-full flex flex-col items-center">
            <h3 class="text-xl md:text-4xl font-bold text-white text-center mt-10">
              Suitable for any type of
              <br />lot you decide
            </h3>
            <div class="relative flex-1 w-full mt-8 h-[300px]">
              <img 
                src="../assets/images/Vector.png"
                alt="Chart" 
                class="w-full h-80 object-cover"
              />
            </div>
          </div>
        </div>

        <!-- Experience Box -->
        <div class="rounded-3xl overflow-hidden group relative h-[500px] md:h-[450px]">
          <div class="absolute inset-0 bg-white/10 backdrop-blur-md group-hover:bg-white/20 transition-all duration-300"></div>
          <div class="relative z-10 p-6 md:p-8 h-full flex flex-col items-center">
            <h3 class="text-xl md:text-4xl font-bold">
              <span class="text-[#FFB800]">5+ years</span>
              <span class="text-white"> of professional</span>
              <br />
              <span class="text-white">experience</span>
            </h3>
            <div class="relative flex-1 w-full mt-8 h-[300px]">
              <img 
                src="../assets/images/image14.svg"
                alt="Number 5" 
                class="w-full h-full object-contain"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

:root {
  font-family: 'Inter', sans-serif;
}

@supports (backdrop-filter: blur(12px)) {
  .backdrop-blur-md {
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
  }
}
</style>