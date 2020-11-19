<template>
  <div class="h-full min-h-screen">
    <Navbar></Navbar>
    <Nuxt />
  </div>
</template>

<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";

.page-enter-active,
.page-leave-active {
  transition: opacity 0.25s;
}
.page-enter,
.page-leave-to {
  opacity: 0;
}

.indent {
  text-indent: 2em;
}

/* 
  .home-enter-active, .home-leave-active { animation: fadeInRight .5s; }
  .home-enter, .home-leave-active { animation: fadeOutLeft .5s;}

  .page-enter-active,
  .page-leave-active {
    transition-property: opacity;
    transition-timing-function: ease-in-out;
    transition-duration: 500ms;
  }
  .page-enter,
  .page-leave-to {
    opacity: 0;
  } */

html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}
</style>

<script>
import Navbar from '~/components/Navbar'
// import Footer from '~/components/Footer'

export default {
    components: {
    Navbar,
    // Footer
  },
  data () {
    return {
      items: [
      ]
    }
  }
}
</script>
