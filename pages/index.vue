<template>
    <div class="min-h-screen">

      

      <div class="antialiased text-blue-900 w-screen px-8 xl:w-2/3 mt-4 mx-auto bg-white sm:mt-12">
      <div class="sm:grid sm:grid-cols-2">
        <div class="hidden sm:block">
          <img class="overflow-auto rounded-full w-auto h-auto object-cover" src="/photos/_DSC2428.png" alt="">
        </div>
  
        <div class="flex flex-wrap justify-center content-center">
          <div class="block h-auto sm:m-8">
            <div class="sm:border-l-2 border-blue-900 sm:pl-2 pt-2 pb-4 mb-4">
              <div class="text-blue-900 text-2xl" >
                Hello,
              </div>
              <div class="text-blue-900 mb-4" >
                Thanks for stopping by! My name is John Church. I'm a student graduating from Claremont Mckenna College this spring. 
              </div>
              <div class="text-blue-900" >
                During my time in college I have studied computer science, philosophy, French, and Arabic. I have been the 
                Director of Internal Affairs on the top model UN team on the West Coast, the executive officer for a newspaper, and the principal developer for a real estate fintech startup. In short, I believe that the best education is an interdisciplinary one. I bring a wide variety of experiences and skills to any project that I work on. 
              </div>
            </div>
        <div class="flex flex-wrap align-center justify-center mx-auto w-2/3">
          <div class="w-full sm:w-auto sm:mx-4 flex justify-center align-center"><nuxt-link to="/experience" aria-label="Experience" title="Experience" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-4">My Experience</nuxt-link></div>
          <div class="w-full sm:w-auto sm:mx-4 flex justify-center align-center">
            <nuxt-link to="/about" aria-label="About" title="About" class="font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-4">About Me</nuxt-link>
          </div>  
        </div> 
          </div>
        </div>
      </div>
      


    </div>
    </div>
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

.stripes {
  background-color: #ffffff;
background-image: url("data:image/svg+xml,%3Csvg width='6' height='6' viewBox='0 0 6 6' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%232a4365' fill-opacity='1' fill-rule='evenodd'%3E%3Cpath d='M5 0h1L0 6V5zM6 5v1H5z'/%3E%3C/g%3E%3C/svg%3E");
/* background-color: #ffffff;
background-image: url("data:image/svg+xml,%3Csvg width='12' height='16' viewBox='0 0 12 16' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M4 .99C4 .445 4.444 0 5 0c.552 0 1 .45 1 .99v4.02C6 5.555 5.556 6 5 6c-.552 0-1-.45-1-.99V.99zm6 8c0-.546.444-.99 1-.99.552 0 1 .45 1 .99v4.02c0 .546-.444.99-1 .99-.552 0-1-.45-1-.99V8.99z' fill='%232a4365' fill-opacity='1' fill-rule='evenodd'/%3E%3C/svg%3E"); */
}

</style>
