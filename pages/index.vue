<template>
    <section class="relative">

      

      <div class="relative antialiased text-blue-900 w-screen px-8 xl:w-2/3 mt-4 mx-auto sm:mt-32 z-10">
      <div class="sm:grid sm:grid-cols-2">
        <div class="hidden sm:block">

          <img class="overflow-auto rounded-full w-auto h-auto object-cover" src="/photos/profile.png" alt="">
        </div>
  
        <div class="flex flex-wrap justify-center content-center">
          <div class="block h-auto sm:m-8">
            <div class="sm:border-l-2 border-blue-900 sm:pl-2 pt-2 pb-4 mb-4">
              <div class="text-blue-900 text-2xl mb-2 sm:mb-4" >
                Hello,
              </div>
              <div class="text-blue-900 mb-4" >
                <p class="">Thanks for stopping by! My name is John Church. I'm a student graduating from Claremont McKenna College this spring. </p>
              </div>
              <div class="text-blue-900" >
                During my time in college, I have studied computer science, philosophy, French, and Arabic. I have been the 
                Director of Internal Affairs on the top model UN team on the West Coast, the executive officer for a newspaper, and the principal developer for a real estate fintech startup. In short, I believe that the best education is an interdisciplinary one. I bring a wide variety of experiences and skills to any project that I work on. 
              </div>
            </div>
          </div>
        </div>
      </div>
      
        <div class="flex flex-wrap align-center justify-center sm:mx-auto w-full sm:w-2/3 mt-4 sm:mt-10">
          <div class="mx-2 flex justify-center align-center"><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-small sm:font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-4">My Experience</nuxt-link></div>
          <div class="mx-2 flex justify-center align-center">
            <nuxt-link to="/about" aria-label="About" title="About" class="font-small sm:font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-4">About Me</nuxt-link>
          </div>  
        </div> 
        <div class="flex flex-wrap align-center justify-center sm:mx-auto w-full sm:w-2/3 mt-2">
          <div class="mx-2 flex justify-center align-center"><a href="https://github.com/John-Church" aria-label="Experience" title="Experience" class="flex justify-center align-center font-small sm:font-medium tracking-wide text-purple-900 transition-colors duration-200 hover:bg-purple-900 hover:text-white hover:border-white border font-extralight border-purple-900 p-1 px-2 mb-4">Github <svg class="mt-1 ml-1 justify-center align-center h-4 w-4 stroke-current inline fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg></a></div>
          <div class="mx-2 flex justify-center align-center"><a href="https://www.linkedin.com/in/j-church/" aria-label="Experience" title="Experience" class="flex justify-center align-center font-small sm:font-medium tracking-wide text-blue-700 transition-colors duration-200 hover:bg-blue-700 hover:text-white hover:border-white border font-extralight border-blue-700 p-1 px-2 mb-4">LinkedIn <svg class="mt-1 ml-1 justify-center align-center h-4 w-4 stroke-current inline fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg></a></div>
        </div>
      </div>


    <!-- <div class="custom-shape-divider-bottom-1605773880 hidden md:block">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="text-gray-200 fill-current"></path>
    </svg>
</div> -->
    </section>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  async asyncData({ $content, params }) {
    const intro = await $content('intro').fetch()

    return { intro }
  },
}
</script>

<style>

.custom-shape-divider-bottom-1605773880 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
    z-index: 0 !important;
}

.custom-shape-divider-bottom-1605773880 svg {
    position: relative;
    display: block;
    width: calc(221% + 1.3px);
    height: 235px;
}
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.nuxt-content p {
  @apply mb-4;
  text-indent: 32px;
}

.layout-enter-active, .layout-leave-active {
  transition: opacity .5s
}
.layout-enter, .layout-leave-active {
  opacity: 0
}

</style>
