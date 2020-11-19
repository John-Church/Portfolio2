<template>
<div class="min-h-screen w-screen">

<div class="h-72">
  <div class="sm:w-2/3 mx-auto mt-4 bg-white px-4 sm:mt-16">
  <div class="mb-12">
      <div class="mb-4">  
          <p class="text-2xl text-blue-900 font-bold">
          </p>
          <div class="border-blue-900 border w-full pl-4 my-2 text-blue-900"></div>
        <p class="text-blue-900">I'm a student from Claremont McKenna College in Southern California who loves hiking, hard problems, and getting lost in interesting places.</p>
          <div class="border-blue-900 border w-full pl-4 my-2"></div>
        
        </div>
      <img src="/photos/508791A7-0871-4ECE-A31C-4B51C28EAC2A_1_105_c.jpeg" alt="Photo of me in a tree.">
          <div class="w-full pl-4 my-2 mt-4"></div>
          <div class="px-4 pt-2 pb-2">
          <div class="flex flex-wrap align-middle">
            <p class="text-blue-900 font-medium pt-1 clear-right sm:clear-none">Tell me a bit more about...</p>
          <button @click="academics = !academics, me = false, work = false" type="button" class="m-1 sm:my-0 sm:mx-2 border-blue-900 border inline-block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">
            <p class="float-left">Academics</p>
            </button>
          <button @click="work = !work, academics = false, me = false" type="button" class="m-1 sm:my-0 sm:mx-2 border-blue-900 border inline-block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">
            <p class="float-left">Work</p>
            </button>
          <button @click="me = !me, academics = false, work = false" type="button" class="m-1 sm:my-0 sm:mx-2 border-blue-900 border inline-block font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white font-extralight border-blue-900 p-1">
            <p class="float-left">Yourself</p>
            </button>
          </div>
      </div>
          <div v-if="academics" class="inline-block text-blue-900 mx-4">
            <p class="font-bold text-2xl border-b border-blue-900">Academics</p>
            <p class="my-2">
              My computer science coursework has included:
              <ul class="list-disc ml-8">
              <li>data structures, </li>
              <li>discrete mathematics, </li>
              <li>graphing algorithms and </li>
              <li>computer networking </li>
              </ul>
              among other topics. My work in discrete mathematics has included an extended segment on encryption theory and my work in computer networking has included principles, protocols, implementation, and analysis. My training in philosophy has focused mainly on classical philosophy, ethics, and epistemology. I have taken multiple courses on bias and epistemic ethics specifically.
            </p>
            <p class="my-2 indent">
              I've spent 2 years studying Arabic (modern standard) including studying in Tunisia, I've studied to proficiency in French, and I've competed on and been elected Director of Internal Affairs and served as joint crisis training manager on the 5th best Model UN club in the country. (Best on the West Coast, and 6 time world champions.) 
            </p>
            <p class="my-2 indent">
              My favorite courses thus far have included classical philosophy, Just War Theory, graphing algorithms, and discrete mathematics. In case you happen to be curious, I'd consider my beliefs to be generally inline with an Aristotelian on most philosophical matters and an individualist just war theorist.
            </p>

            <div>
              <p class="my-2 border-b border-blue-900 font-bold">
                Honors 
              </p>
              <p class="my-2 clear-left">
                McKenna Scholar (2017), Appel Fellow (2018), Summit Fellow (2019), 1st Place Gould Humanities Competition (2020)
              </p>
            </div>
            <!-- <div>
              <p class="my-2 border-b border-blue-900 font-bold">
                Sample Work
              </p>
              <p class="my-2 clear-left flex flex-wrap mt-2">
                <nuxt-link to="/examsample" aria-label="examsample" title="examsample" class="mr-2 font-small sm:font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-2">Applied Ethics Exam</nuxt-link>
                <nuxt-link to="/essaysample" aria-label="essaysample" title="essaysample" class="mr-2 font-small sm:font-medium tracking-wide text-blue-900 transition-colors duration-200 hover:bg-blue-900 hover:text-white hover:border-white border font-extralight border-blue-900 p-1 px-2 mb-2">Essay Sample: </nuxt-link>
              </p>
            </div> -->
          </div>

          <div v-if="work" class="inline-block text-blue-900 mx-4">
            <p class="font-bold text-2xl border-b border-blue-900">Work</p>
            <p class="my-2 indent">
              During my freshman summer working at Agilefield, I self-taught myself the Flask framework, database management with SQL and PostgreSQL, and API requests in order to fulfill tasks given to me by the CTO. During my sophomore summer, I assisted in the development of the privacy compliance portal for a blockchain-enabled privacy compliance company, ComplyUSA. Most recently, I have worked remotely to build the Django backend and frontend and assist with branding for RentWink, a real estate technology startup in Florida. I have also enjoyed advancing my abilities through independent studies into data science, machine learning, and web design (including learning design software like Adobe Illustrator and XD).
            </p>
            <p class="my-2 indent">
              I also worked at the Roberts Environmental Center, a research institute at Claremont Mckenna College, during the school year. I worked as an analyst my freshman year and worked as a manager my sophmore and junior years. I led a team of student anlysts working on problems such as soil carbon storage in relation to landscaping choices, water quality testing on Mount Baldy, and policy writing for the Forest Service. In my capcity as manager, it was my responsibility to gauge client needs and plan projects accordingly, direct my team in conducting research, and convey technical findings to stakeholders.  
            </p>
            <p class="my-2 indent">
              I love working with teams of passionate poeple in a fast paced collaborative environments. I enjoy solving problems with ambiguous or difficult to define goals but only when the team itself has concrete values and a mission.
            </p>
            </div>

          <div v-if="me" class="inline-block text-blue-900 mx-4">
            <p class="font-bold text-2xl border-b border-blue-900">Me</p>
            <p class="my-2 indent">
              
            </p>
            <div class="flex flex-wrap">

              <img class="p-4 w-full sm:w-1/2" src="/photos/823FBF1A-DFDE-4E8B-AB0C-34B62D322C31_1_105_c.jpeg" alt="">
              <p class="p-4 w-full sm:w-1/2" >
              I'm a big fan of:
              <ul class="list-disc ml-8">
                  <li>Hiking</li>
                  <li>Xcountry biking</li>
                  <li>People</li>
                  <li>Lists</li>
                  <li>Watercolors</li>
                  <li>Whatever "Still Woozy" released in a given month</li>
              </ul>
               </p>
              <p class="p-4 w-full sm:w-1/2" >
              When I'm not trying to figure out what to put in the "about me" section of my portfolio or locked inside due to Covid restrictions, you could find me out with friends, on a camping trip, trying to paint with watercolors (very poorly), or trying to learn another instrument (only slightly less poorly than my painting)
              </p>
              <img class="p-4 w-full sm:w-1/2" src="/photos/IMG_0583.jpeg" alt="">

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
      isMenuOpen: false,
      academics: false,
      work: false,
      me: false,
    }
  },
}
</script>

<style>
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

</style>
