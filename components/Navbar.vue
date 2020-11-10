<template>
  <div
    class="px-4 py-5 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 antialiased"
  >
    <div class="relative flex items-center justify-between">
      <nuxt-link to="/" aria-label="John Church" title="John Church" class="inline-flex items-center">
      <span class="text-xl tracking-wide text-blue-900 bg-white transition-colors">John Church</span>
      </nuxt-link>
      <ul class="flex items-center hidden space-x-8 lg:flex">
        <ul class="flex items-center hidden space-x-8 lg:flex">
      <li><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1">Experience</nuxt-link></li>
      <li><nuxt-link to="/about" aria-label="About" title="About" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1">About Me</nuxt-link></li>
      <li><nuxt-link to="/contact" aria-label="Contact" title="Contact" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border-b font-extralight border-blue-900 p-1">Contact</nuxt-link></li>
    </ul>
      </ul>
      <div class="lg:hidden">
        <button
          aria-label="Open Menu"
          title="Open Menu"
          class="p-2 -mr-1 transition duration-200 rounded focus:outline-none focus:shadow-outline hover:bg-blue-300 focus:bg-blue-300"
          @click="isMenuOpen = true"
        >
          <svg class="w-5 text-gray-600" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M23,13H1c-0.6,0-1-0.4-1-1s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,13,23,13z"
            ></path>
            <path
              fill="currentColor"
              d="M23,6H1C0.4,6,0,5.6,0,5s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,6,23,6z"
            ></path>
            <path
              fill="currentColor"
              d="M23,20H1c-0.6,0-1-0.4-1-1s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,20,23,20z"
            ></path>
          </svg>
        </button>
        <div v-if="isMenuOpen" class="absolute top-0 right-0 w-auto">
          <div class="px-10 pt-4">
            <div class="flex items-center justify-between mb-4">
                <button
                  aria-label="Close Menu"
                  title="Close Menu"
                  class="p-2 -mt-2 float-left -mr-2 transition duration-200 rounded hover:bg-gray-200 focus:bg-gray-200 focus:outline-none focus:shadow-outline"
                  @click="isMenuOpen = false"
                >
                  <svg class="w-5 text-gray-600" viewBox="0 0 24 24">
                    <path
                      fill="currentColor"
                      d="M19.7,4.3c-0.4-0.4-1-0.4-1.4,0L12,10.6L5.7,4.3c-0.4-0.4-1-0.4-1.4,0s-0.4,1,0,1.4l6.3,6.3l-6.3,6.3 c-0.4,0.4-0.4,1,0,1.4C4.5,19.9,4.7,20,5,20s0.5-0.1,0.7-0.3l6.3-6.3l6.3,6.3c0.2,0.2,0.5,0.3,0.7,0.3s0.5-0.1,0.7-0.3 c0.4-0.4,0.4-1,0-1.4L13.4,12l6.3-6.3C20.1,5.3,20.1,4.7,19.7,4.3z"
                    ></path>
                  </svg>
                </button>
              </div>
            </div>
            <nav>
              <ul class="space-y-4">
                <li>
                  <a
                    href="/"
                    aria-label="Our product"
                    title="Our product"
                    class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:text-deep-purple-accent-400"
                    >Product</a
                  >
                </li>
                <li>
                  <a
                    href="/"
                    aria-label="Our product"
                    title="Our product"
                    class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:text-deep-purple-accent-400"
                    >Features</a
                  >
                </li>
                <li>
                  <a
                    href="/"
                    aria-label="Product pricing"
                    title="Product pricing"
                    class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:text-deep-purple-accent-400"
                    >Pricing</a
                  >
                </li>
                <li>
                  <a
                    href="/"
                    aria-label="About us"
                    title="About us"
                    class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:text-deep-purple-accent-400"
                    >About us</a
                  >
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </div>
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



@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>
