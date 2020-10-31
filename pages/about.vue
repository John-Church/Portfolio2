<template>
<div class="min-h-screen">
    <div class="w-screen px-8 xl:w-2/3 mx-auto mt-16">
    <p class="text-gray-100 antialiased text-lg mt-2">
      My name is John Church. I'm a student of philosophy and computer science currently attending Claremont Mckenna College in Southern California.
    </p>
   <div class="flex flex-wrap">
      <img src="/photos/823FBF1A-DFDE-4E8B-AB0C-34B62D322C31_1_105_c.jpeg" alt="">
      <img src="/photos/131192FF-AE11-4514-9A0F-D8E6BB13EC4A_1_105_c.jpeg" alt="">
      <img src="/photos/508791A7-0871-4ECE-A31C-4B51C28EAC2A_1_105_c.jpeg" alt="">
      <img src="/photos/A5F43326-0DB4-4A8D-A06E-B0A722357559_1_105_c.jpeg" alt="">
      <img src="/photos/E8F927EE-A542-45DE-BEC1-3191F22DCBDA_1_105_c.jpeg" alt="">
   </div>

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
