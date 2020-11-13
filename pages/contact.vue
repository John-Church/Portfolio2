<template>
<div class="w-screen px-8 xl:w-2/3 mx-auto mt-16 flex justify-center h-screen">
<!-- component -->
<form class="w-full max-w-lg"
name="contact" 
  action="/thanks" 
  method="post" 
  netlify
  netlify-honeypot="bot-field"
  >
  <div class="flex flex-wrap -mx-3 mb-6">
    <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
    <input type="hidden" name="form-name" value="contact" />
      <label class="block  tracking-wide text-blue-900 text-xs  mb-2" for="name">
        Name
      </label>
      <input class="appearance-none block w-full bg-gray-200 text-blue-900 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:bg-white" id="name" name="name" required type="text" placeholder="Jane">
    </div>
  </div>
  <div class="flex flex-wrap -mx-3 mb-6">
    <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
      <label class="block  tracking-wide text-blue-900 text-xs  mb-2" for="email">
        E-mail
      </label>
      <input class="appearance-none block w-full bg-gray-200 text-blue-900 border border-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:bg-white focus:border-gray-500" id="email" type="email" name="email" required>
    </div>
  </div>
  <div class="flex flex-wrap -mx-3 mb-6">
    <div class="w-full px-3">
      <label class="block  tracking-wide text-blue-900 text-xs  mb-2" for="subject">
        Subject
      </label>
      <input class="appearance-none block w-full bg-gray-200 text-blue-900 border border-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:bg-white focus:border-gray-500" id="subject" type="subject" name="subject" required>
    </div>
  </div>
  <div class="flex flex-wrap -mx-3 mb-6">
    <div class="w-full px-3">
      <label class="block  tracking-wide text-blue-900 text-xs  mb-2" for="message">
        Message
      </label>
      <textarea class=" no-resize appearance-none block w-full bg-gray-200 text-blue-900 border border-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:bg-white focus:border-gray-500 h-48 resize-none" id="message" name="message" required></textarea>
    </div>
  </div>
  <div class="md:flex md:items-center">
    <div class="md:w-1/3">
      <button class="shadow bg-blue-900 hover:bg-gray-400 focus:shadow-outline text-white  py-2 px-4 rounded" type="submit" value="Send Message">
        Send
      </button>
    </div>
    <div class="md:w-2/3"></div>
  </div>
</form>

  </div>
</template>
<script>
import axios from "axios";

export default {
}
</script>




<style>

</style>