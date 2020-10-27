<template>
<div class="">
    <div class="w-1/3 mx-auto mt-16">
    <p class="text-gray-100 antialiased text-xl">
      Claremont Mckenna College
    </p>
    <p class="text-gray-100 antialiased text-lg mt-2">
      My name is John Church. I'm a student of philosophy and computer science currently attending Claremont Mckenna College in Southern California. 
    </p>
    </div>
</div>
</template>

<script>
export default {
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
