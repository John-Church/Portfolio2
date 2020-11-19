<template>
  <!-- <div
    class="px-4 py-5 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 antialiased"
  >
    <div class="relative flex items-center justify-between">
      <nuxt-link to="/" aria-label="John Church" title="John Church" class="inline-flex items-center">
      <span class="text-xl tracking-wide text-blue-900 bg-white transition-colors">John Church</span>
      </nuxt-link>
      <ul class="flex items-center hidden space-x-8 lg:flex">
        <ul class="flex items-center hidden space-x-8 lg:flex">
      <li><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">Experience</nuxt-link></li>
      <li><nuxt-link to="/about" aria-label="About" title="About" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">About Me</nuxt-link></li>
      <li><nuxt-link to="/contact" aria-label="Contact" title="Contact" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">Contact</nuxt-link></li>
    </ul>
      </ul>
      <div class="lg:hidden">
        <button class="block h-6 w-6">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7" />
          </svg>
        </button>
        <div class="bg-white rounded-lg">
          <ul>
            <li><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">Experience</nuxt-link></li>
            <li><nuxt-link to="/about" aria-label="About" title="About" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">About Me</nuxt-link></li>
            <li><nuxt-link to="/contact" aria-label="Contact" title="Contact" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-3">Contact</nuxt-link></li>
          </ul>
        </div> -->

  <header class="">
    <div class="flex items-center justify-between px-4 py-2 w-screen px-8 xl:w-2/3 mx-auto">
      <div>
        <nuxt-link to="/" aria-label="John Church" title="John Church" class="inline-flex items-center">
        <span class="text-xl tracking-wide text-blue-900 bg-white transition-colors">John Church</span>
        </nuxt-link>
      </div>

      <div class="hidden sm:block">
        <ul class="flex items-center space-x-8">
        <li><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-2">Experience</nuxt-link></li>
        <li><nuxt-link to="/about" aria-label="About" title="About" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-2">About Me</nuxt-link></li>
        <li><nuxt-link to="/contact" aria-label="Contact" title="Contact" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1 px-2">Contact</nuxt-link></li>
        </ul>
      </div>



      <div class="sm:hidden">
        <button @click="isMenuOpen = !isMenuOpen" type="button" class="block h-6 w-6 text-blue-900">
            
            <svg xmlns="http://www.w3.org/2000/svg" class="fill-current" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />   
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7" />
            </svg>
          </button>
      </div>
    </div>
   <transition name="dropdown">
    <div :class="isMenuOpen ? 'block' : 'hidden'" class="px-4 pt-2 pb-2 bg-gray-200">
        <nuxt-link to="/experience" aria-label="Experience" title="Experience" class="block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">Experience</nuxt-link>
        <nuxt-link to="/about" aria-label="About" title="About" class="block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">About Me</nuxt-link>
        <nuxt-link to="/contact" aria-label="Contact" title="Contact" class="block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">Contact</nuxt-link>
    </div>
    </transition>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
};
</script>

<style>
.NuxtLogo {
  animation: 1s appear;
  margin: auto;
};
.nuxt-link-active {
    @apply bg-blue-900 text-white border-blue-900
}
.nuxt-link-exact-active {
    @apply bg-blue-900 text-white border-blue-900
}

.dropdown-enter,
.dropdown-leave-to {
  opacity: 0;
}

.dropdown-enter-to,
.dropdown-leave {
  opacity: 1;
  
}

.dropdown-enter-active,
.dropdown-leave-active {
  transition: all 0.3s ease-out;
  transform-origin: top center;
}




@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>
