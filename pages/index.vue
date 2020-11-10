<template>
    <div class="min-h-screen">

      <div class="antialiased text-blue-900 w-screen px-8 xl:w-2/3 mx-auto mt-16">
        <nuxt-content :document="intro" />
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

</style>
