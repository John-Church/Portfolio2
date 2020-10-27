<template>
<div class="" id="app">
    <div class="w-screen px-8 xl:w-2/3 mx-auto mt-16">
    
      <div>  
        <p class="text-2xl text-white font-bold">
          Education
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

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

      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Experience
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

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

      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Leadership
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

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
      <div class="pt-4">  
        <p class="text-2xl text-white font-bold">
          Skills
        </p>
        <div class="border-white border w-full pl-4"></div>
      </div>

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

    <!-- buffer -->
    <div class="h-24 w-full"></div>

</div>
</template>

<script>
import nuxtConfig from '~/nuxt.config'
export default {
  data() {
    return {
    Toggles:
    {
      computerLanguages: true,
      frameworks: true,
      frontend: true,
      backend: true,
      softSkills: true,
      projectManagement: true,
      languages: true,
    },

    Education: 
    [
      {
        title: 'Claremont Mckenna College',
        location: 'Claremont, CA',
        startDate: 'May 2021',
        endDate: 'May 2020',
        subscript: 'Bachelor of Arts in Philosophy with a Sequence in Computer Science',
        content: [
          'GPA: 3.6/4.0',
          'Awards: McKenna Scholar (2017), Appel Fellow (2018), Summit Fellow (2019), 1st Place Gould Humanities Competition (2020)',
          'Relevant Coursework: Principles of Computer Science, Data Structures, Computer Networking, Discrete Math, Graphing Algorithms, Ethics, Psychology and Philosophy of Bias in Research',
        ]
      },
    ],

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

    SkillsAndInterests: 
    {
      skills:
        {
          codingLanguages: 
          [
            'Python',
            'Java',
            'C++',
            'Javascript',
            'CSS',
            'HTML',
            'SQL',
          ],
          frameworks: 
          [
            'Django',
            'Flask',
            'Vue',
            'Nuxt',
            'Tailwind',
            'Bootstrap',
          ],
          computerScience:
          [
            'Algorithms',
            'Computer Networking',
            'Data Structures',
            'Graphing Algorithms',
            'JAMstack',
            'Database Design',
          ],
          softSkills:
          [
            'Public Speaking',
            'Project Management',
          ],
          design:
          [
            'Photoshop',
            'Illustrator',
            'InDesign',
            'Web Design',
          ],
          misc:
          [
            'Excel',
            'PostgreSQL',
          ],

        },
      languages:
        [
          'English (native)',
          'French (working proficiency)',
          'Arabic (MS, intermediate)',
          'Latin (basic translation)',
        ],
      interests:
        [
          'hiking',
          'typography',
          'watercolor painting',
          'music (mostly Alternative)',
          'running',
          'classics',
        ],
    }

  }
},
  computed: {
    // a computed getter
    reversedMessage: function () {
      // `this` points to the vm instance
      return this.message.split('').reverse().join('')
    },
    SkillsList: function () {
      // `this` points to the vm instance
      return this.message.split('').reverse().join('')
    },
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
</style>
