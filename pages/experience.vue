<template>
<div class="" id="app">
    <div class="w-screen px-8 xl:w-2/3 mx-auto mt-16">
    
      <div>  
        <p class="text-2xl text-white font-bold">
          Education
        <span>
          <button @click="educationToggle = !educationToggle" class="text-white text-sm mx-2 p-1">
            <svg width="18" height="17" class="antialiased">
              <polyline points="
                2 10
                8 16
                16 10
              "></polyline>
            </svg>
          </button>
        </span>
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

      <div v-if="educationToggle">
        <div v-for="(item) in Education" :key="item" class="clear-left">
            <p class="text-gray-100 antialiased text-lg mt-2 float-left font-bold">
              {{ item.title }}<span class="hidden md:inline-block">{{ ', ' + item.location }}</span>
            </p>
            <p class="text-gray-100 antialiased italic mt-2 float-right">
              {{ item.startDate + " " + item.endDate }}
            </p>
            <p class="text-gray-100 antialiased italic clear-left text-sm">
              {{ item.subscript }}
            </p>
            <ul class="list-disc ml-8">
              <li v-for="(content) in item.content" :key="content" class="text-gray-100 antialiased text-sm">
                {{ content }}
              </li>
            </ul>
        </div>
      </div>

      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Experience
          <span>
          <button @click="experienceToggle = !experienceToggle" class="text-white text-sm mx-2 p-1">
            <svg width="18" height="17" class="antialiased">
              <polyline points="
                2 10
                8 16
                16 10
              "></polyline>
            </svg>
          </button>
        </span>
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

      <div v-if="experienceToggle">
      <div v-for="(item) in Experience" :key="item" class="clear-left">
          <p class="text-gray-100 antialiased text-lg mt-2 float-left font-bold">
            {{ item.title}}<span class="hidden md:inline-block">{{ ', ' + item.location }}</span>
          </p>
          <p class="text-gray-100 antialiased italic mt-2 float-right">
            {{ item.startDate + " " + item.endDate }}
          </p>
          <p class="text-gray-100 antialiased italic clear-left text-sm">
            {{ item.subscript }}
          </p>
          <ul class="list-disc ml-8">
            <div v-for="(content) in item.content" :key="content" class="text-gray-100 antialiased text-sm">
              <div v-if="Array.isArray(content)">
                <ul class="list-disc ml-8">
                  <li v-for="subitem in content" :key="subitem" class="">
                    {{ subitem }}
                  </li>
                </ul>
              </div>
              <li v-else>{{ content }}</li>
            </div>
          </ul>
      </div>
      </div>

      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Leadership
          <span>
          <button @click="leadershipToggle = !leadershipToggle" class="text-white text-sm mx-2 p-1">
            <svg width="18" height="17" class="antialiased">
              <polyline points="
                2 10
                8 16
                16 10
              "></polyline>
            </svg>
          </button>
        </span>
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

    <div v-if="leadershipToggle">
    <div v-for="(item) in Leadership" :key="item" class="clear-left">
        <p class="text-gray-100 antialiased text-lg mt-2 float-left font-bold">
          {{ item.title}}<span class="hidden md:inline-block">{{ ', ' + item.location }}</span>
        </p>
        <p class="text-gray-100 antialiased italic mt-2 float-right">
          {{ item.startDate + " " + item.endDate }}
        </p>
        <p class="text-gray-100 antialiased italic clear-left text-sm">
          {{ item.subscript }}
        </p>
        <ul v-if="item.content != undefined && item.content.length != 0" class="float-left list-disc ml-8">
          <li v-for="(content) in item.content" :key="content" class="text-gray-100 antialiased text-sm">
            {{ content }}
          </li>
        </ul>
      </div>
    </div>


      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Skills
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

<div class="flex flex-wrap">
      <div v-for="(toggle) in Toggles" :key='toggle.name'>
        <button 
        @click="toggle.value = !toggle.value" 
        :class="{ 'bg-gray-100 text-blue-900 border-blue-900': toggle.value}"
        class="font-medium mr-2 tracking-wide text-gray-100 transition-colors duration-200 hover:bg-gray-100 hover:text-blue-900 hover:border-blue-900 border-b font-extralight border-gray-100 p-1"
        >
        {{ toggle.name }}
        </button>
      </div>
</div>

    <div class="h-auto lg:h-48">
      <div class="flex flex-wrap mt-4">
        <div v-for="(item) in SkillsList" :key="item" class="text-gray-100 antialiased m-1 p-1 border border-white">
            {{ item }} 
          </div>
      </div>
    </div>

    </div>

    <!-- buffer -->
    <div class="h-48 w-full"></div>

</div>
</template>

<script>
import nuxtConfig from '~/nuxt.config'
export default {
  data() {
    return {
    educationToggle: true,
    Education: 
    [
      {
        title: 'Claremont Mckenna College',
        location: 'Claremont, CA',
        startDate: 'May 2021',
        endDate: 'May 2020',
        subscript: 'Bachelor of Arts in Philosophy with a Sequence in Computer Science',
        content: [
          'Awards: McKenna Scholar (2017), Appel Fellow (2018), Summit Fellow (2019), 1st Place Gould Humanities Competition (2020)',
          'Relevant Coursework: Principles of Computer Science, Data Structures, Computer Networking, Discrete Math, Graphing Algorithms, Ethics, Psychology and Philosophy of Bias in Research',
        ]
      },
    ],
    experienceToggle: true,
    Experience: 
    [
      {
        title: 'Roberts Environmental Center',
        location: 'Claremont, CA',
        startDate: 'December 2017',
        endDate: 'May 2020',
        subscript: 'Manager of the Conservation Team',
        content: [
          'Manage team of 7 students and jointly supervise highly selective research institute of 39 students',
          'Relate scientific findings to board of trustees and shareholders, coordinate research, plan future projects',
          'Gain considerable project management experience through leading projects such as:',
            ['Policy gap analysis for the US Forest Service concerning through-hiking to aid creation of policy which will become standard on Pacific Crest Trail upon completion',
            'Study on effects of landscaping on A-Horizon soil carbon storage in order to advise college on sustainable landscaping choices and advance body of research',],
        ]
      },
      {
        title: 'RentWink',
        location: 'Tampa, FL',
        startDate: 'July 2019',
        endDate: 'Present',
        subscript: 'Part-Time Software Engineer',
        content: [
          'Advised CEO on technical viability of project goals and most cost-effective implementations',
          'Assisted in planning and implementation of backend PostgreSQL database for Django web app',
        ]
      },
      {
        title: 'ComplyUSA',
        location: 'Phoenix, AZ',
        startDate: 'June 2019',
        endDate: 'July 2019',
        subscript: 'Summer Intern',
        content: [
          'Assisted in development of the partner privacy portal for a cutting edge privacy compliance company',          
        ]
      },
      {
        title: 'AgileField',
        location: 'Scottsdale, AZ',
        startDate: 'July 2018',
        endDate: 'August 2018',
        subscript: 'Summer Intern',
        content: [
          'Created utility plugin to automate database management tasks for the CTO',
          'Designed and implemented an API monitoring website with Flask and Bootstrap used by entire dev team',
          'Self-taught database management (PostgreSQL, Flask) to meet project goals',
        ]
      },
      {
        title: 'Information Technology Services',
        location: 'Claremont, CA',
        startDate: 'August 2018',
        endDate: 'May 2019',
        subscript: 'Residential technology Assistant',
        content: [
          'Responsible for reporting on and solving technical problems within one dorm at Claremont McKenna',
        ]
      },
      {
        title: 'Claremont Radius',
        location: 'Claremont, CA',
        startDate: 'September 2017',
        endDate: 'December 2019',
        subscript: 'Executive Officer',
        content: [
          'Create marketing material, logos, and website graphics to increase engagement and introduce new initiatives',
        ]
      },
      {
        title: 'Robert W. Baird and Company',
        location: 'Phoenix, AZ',
        startDate: 'July 2017',
        endDate: '',
        subscript: 'Marketing and Financial Services Intern',
        content: [
          'Designed a website and written material while learning about quantitative and qualitative trading methods',
        ]
      },
    ],
    leadershipToggle: true,
    Leadership: 
    [
      {
        title: 'Model United Nations',
        location: 'Claremont, CA',
        startDate: 'September 2017',
        endDate: 'Present',
        subscript: 'Director of Internal Affairs',
        content: [
        ]
      },
      {
        title: 'Outdoor Initiative',
        location: 'Claremont, CA',
        startDate: 'September 2018',
        endDate: 'Present',
        subscript: 'Leader',
        content: [
        ]
      },
      {
        title: 'Collegiate Track',
        location: 'Claremont, CA',
        startDate: 'September 2018',
        endDate: 'Present',
        subscript: 'Varsity Member in the 400 and 800-meter races',
        content: [
        ]
      },
    ],

  Toggles:
    {
      // projectManagement: {
      //   name: 'Project Management', 
      //   value: false,
      //   content:
      //   []
      //   },
      computerLanguages: {
        name: 'Computer Languages', 
        value: false,
        content:
        [
            'CSS',
            'C++',
            'HTML',
            'Java',
            'Javascript',
            'Python',
            'SQL',
          ],
        },
      frameworks: {
        name: 'Frameworks', 
        value: false,
        content:
        [
            'Bootstrap',
            'Django',
            'Flask',
            'Nuxt',
            'Tailwind',
            'Vue',
          ],
        },
      computerscience: {
        name: 'Computer Science', 
        value: false,
        content:
        [
            'Algorithms',
            'Computer Networking',
            'Data Structures',
            'Database Design',
            'Graphing Algorithms',
            'JAMstack',
          ],
        },
      // frontend: {
      //   name: 'Frontend', 
      //   value: false,
      //   content:
      //   []
      //   },
      // backend: {
      //   name: 'Backend', 
      //   value: false,
      //   content:
      //   []
      //   },
      design: {
        name: 'Design', 
        value: false,
        content:
        [
            'InDesign',
            'Illustrator',
            'Photoshop',
            'Web Design',
          ],
        },
      languages: {
        name: 'Languages', 
        value: false,
        content:
        [
          'Arabic (MS, intermediate)',
          'English (native)',
          'French (working proficiency)',
          'Latin (basic translation)',
        ],
        },
      softSkills: {
        name: 'Soft Skills', 
        value: false,
        content:
        [
            'Project Management',
            'Public Speaking',
          ],
        },
      misc: {
        name: 'Misc.', 
        value: false,
        content:
        [
            'Excel',
            'PostgreSQL',
        ],
        },
    },
    Interests: 
        [
          'classics',
          'hiking',
          'typography',
          'music (mostly Alternative)',
          'running',
          'watercolor painting',
        ],
  }
},
  computed: {
    // a computed getter
    reversedMessage: function () {
      // `this` points to the vm instance
      return this.message.split('').reverse().join('')
    },
    SkillsList: function () {
      var L = []
      var L2 = []
      console.log("hello")
      for (var t in this.Toggles) {
        console.log(this.Toggles[t].name)
        if (this.Toggles[t].value == true) {
          for (var i of this.Toggles[t].content) {
            if (!L.includes(i)) {
              L.push(i)
            }
          } 
          } else {
          for (var i of this.Toggles[t].content) {
            if (!L2.includes(i)) {
              L2.push(i)
            }
          }
        }
      }
      if (L.length == 0) {
        return L2
      } else {
        return L
      }
    },
  },
  methods: {
  },
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

svg {
  stroke: rgb(255, 255, 255);
  stroke-width: 2;
  /* stroke-linecap: round;
  stroke-linejoin: round; */
  fill: none;
}
</style>
