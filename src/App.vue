<script setup>
import HeaderPostfolio from './components/HeaderPostfolio.vue';
import ContactMe from './components/ContactMe.vue';
</script>

<script>
export default {
  data() {
    return {
      toggleA: true,
      toggleB: true,
      list_logo:"bootstrap_logo",
      data_project_intren : {
        company:"Creden Asia Co., Lid.",
        career:"Software Deverloper Internship",
        time:"May. 2021 - Oct. 2021",
        content_card : [
          {
            topic:"Landing Page Development",
            detail_topic : [
              "Write clean and efficient HTML, CSS, and JavaScript code to create beautiful and user-friendly landing pages.",
              "Collaborate with UI/UX designers to deliver landing pages that meet user needs."
            ]
          },
          {
            topic:"API Development",
            detail_topic : [
              "Design and build new APIs based on business requirements.",
              "Write API code in a suitable language (e.g., Lua,Python,Node.js).",
              "Create API documentation for developers."
            ]
          },
          {
            topic:"Developed a Back-Office Project",
            detail_topic : [
              "Developed a back-office system to manage and organize data for a company.",
              "The system was designed to be user-friendly and efficient, allowing users to easily manage their data.",
            ]
          }
        ]
      },
      data_project_software_dev : {
        company:"Creden Asia Co., Lid.",
        career:"Software Deverloper",
        time:"Jun. 2022 - Present.",
        content_card : [
          {
            topic:"Website Development",
            detail_topic : [
              "Website development is a multi-step process that varies depending on the website's complexity and user goals.",
              "Writing code in front-end , back-end. And testing the website across various browsers and devices",
            ]
          },
          {
            topic:"Web scraping",
            detail_topic : [
              "Web scraping refers to the process of automatically extracting data from websites. This data can be in various formats, such as text, images, or even links."
            ]
          },
          {
            topic:"Data Cleaning",
            detail_topic : [
              "Develop code or scripts to clean data based on defined rules.",
              "Thoroughly test the system with various sample datasets to assess performance and accuracy.",
            ]
          }
        ]
      }
    };
  }
}
</script>

<template>
  <div id="app">
    <!-- Navigation Bar -->
    <nav class="flex-no-wrap fixed relative top-0 flex w-full items-center justify-between bg-[#FBFBFB] py-2 shadow-md shadow-black/5 dark:bg-gray-300 dark:shadow-gray/10 lg:flex-wrap lg:justify-start lg:py-4">
      <div class="mx-auto">
        <div class="flex items-center justify-between">
          <div>
            <h1 class="text-sm md:text-base">Phetlada Thongkarn</h1>
          </div>
          <!-- <div>
            <h1 class="text-sm md:text-base">Home | About | Resume | Projects</h1>
          </div> -->
        </div>
      </div>
    </nav>
    <div class="container mx-auto">
      <div class="bg-header">
        <div class="flex items-center justify-center">
          <HeaderPostfolio></HeaderPostfolio>
        </div>
      </div>
      <div class="bg-content-one">
        <div class="box-content">
          <h1 class="topic-content">Education</h1>
          <transition name="slide" appear>
            <div class="side-content" v-if="toggleA">
              <div class="flex items-center justify-center">
                <card>
                  <div class="header-card border-b-4 border-b-indigo-500">
                    <span class="flex justify-between">
                      <svg class="mr-2 h-8 w-8 text-yellow-500" width="24" height="24" viewBox="0 0 24 24"
                        stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                        <path stroke="none" d="M0 0h24v24H0z" />
                        <path d="M8 9l5 5v7h-5v-4m0 4h-5v-7l5 -5m1 1v-6a1 1 0 0 1 1 -1h10a1 1 0 0 1 1 1v17h-8" />
                        <line x1="13" y1="7" x2="13" y2="7.01" />
                        <line x1="17" y1="7" x2="17" y2="7.01" />
                        <line x1="17" y1="11" x2="17" y2="11.01" />
                        <line x1="17" y1="15" x2="17" y2="15.01" />
                      </svg>
                      | 2022
                    </span>
                    King Mongkut’s University of Technology North Bangkok
                  </div>
                  <div class="content-card">
                    <p>Bachelor of technology</p>
                    <p>Information Technology Major</p>
                  </div>
                </card>
              </div>
            </div>
          </transition>
        </div>
      </div>
      <div class="bg-content-work-experience">
        <div class="box-content">
          <transition name="slide" appear>
            <div class="side-content" v-if="toggleB">
              <div class="topic-content text-white">Work Experience</div>
              <div class="decs-topic">
                <span class="flex justify-between text-lg md:text-xl">
                  <svg class="h-8 w-8 text-yellow-500" width="24" height="24" viewBox="0 0 24 24"
                    stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" />
                    <path d="M8 9l5 5v7h-5v-4m0 4h-5v-7l5 -5m1 1v-6a1 1 0 0 1 1 -1h10a1 1 0 0 1 1 1v17h-8" />
                    <line x1="13" y1="7" x2="13" y2="7.01" />
                    <line x1="17" y1="7" x2="17" y2="7.01" />
                    <line x1="17" y1="11" x2="17" y2="11.01" />
                    <line x1="17" y1="15" x2="17" y2="15.01" />
                  </svg>
                  | {{ data_project_intren.time }}
                </span>
                {{ data_project_intren.career }}
                <div class=" md:text-lg text-base">{{ data_project_intren.company }}</div>
              </div>
              <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-10">

                <card v-for="(value,index) in data_project_intren.content_card" :key="value.topic">
                  <img v-if="index == 0" class="rounded" src="./assets/landing-page.webp" />
                  <img v-if="index == 1" class="rounded" src="./assets/task-api.webp" />
                  <img v-if="index == 2" class="rounded" src="./assets/project-backoffice.webp" />
                  <div class="content-card">
                    <span class="flex font-bold font-xl">{{ value.topic }}<a v-if="index == 0" href="https://data.creden.co/"><svg class="h-4 w-4 md:h-6 md:w-6 text-red-500 font-bold"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6" />  <polyline points="15 3 21 3 21 9" />  <line x1="10" y1="14" x2="21" y2="3" /></svg></a></span>
                    <ul class="list-disc text-ellipsis ml-8 text-base">
                      <li v-for="sentence in value.detail_topic">{{ sentence  }}</li>
                    </ul>
                  </div>
                  <div class="bottom-card flex justify-end">
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/html.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/css.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/vue.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/bootstrap.svg" />   

                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/mongodb.svg" />
                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/lua.svg" />

                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/mongodb.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/lua.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/html.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/css.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/vue.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/bootstrap.svg" />
                  </div>
                </card>

              </div>

              <div class="decs-topic mt-10">
                <span class="flex justify-between text-lg md:text-xl">
                  <svg class="h-8 w-8 text-yellow-500" width="24" height="24" viewBox="0 0 24 24"
                    stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" />
                    <path d="M8 9l5 5v7h-5v-4m0 4h-5v-7l5 -5m1 1v-6a1 1 0 0 1 1 -1h10a1 1 0 0 1 1 1v17h-8" />
                    <line x1="13" y1="7" x2="13" y2="7.01" />
                    <line x1="17" y1="7" x2="17" y2="7.01" />
                    <line x1="17" y1="11" x2="17" y2="11.01" />
                    <line x1="17" y1="15" x2="17" y2="15.01" />
                  </svg>
                  | {{ data_project_software_dev.time }}
                </span>
                {{ data_project_software_dev.career }}
                <div class=" md:text-lg text-base">{{ data_project_software_dev.company }}</div>
              </div>
              <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-10">

                <card v-for="(value,index) in data_project_software_dev.content_card" :key="value.topic">
                  <img v-if="index == 0" class="rounded" src="./assets/full-stack.webp" />
                  <img v-if="index == 1" class="rounded" src="./assets/wep-scraping.webp" />
                  <img v-if="index == 2" class="rounded" src="./assets/data-cleansing.webp" />
                  <div class="content-card">
                    <span class="flex font-bold font-xl">{{ value.topic }}<a v-if="index == 0" href="https://data.creden.co/"><svg class="h-4 w-4 md:h-6 md:w-6 text-red-500 font-bold"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6" />  <polyline points="15 3 21 3 21 9" />  <line x1="10" y1="14" x2="21" y2="3" /></svg></a></span>
                    <ul class="list-disc text-ellipsis ml-8 text-base">
                      <li v-for="sentence in value.detail_topic">{{ sentence  }}</li>
                    </ul>
                  </div>
                  <div class="bottom-card flex justify-end">
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/postgresql.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/mongodb.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/lua.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/python.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/html.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/css.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/vue.svg" />
                    <img v-if="index == 0" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/bootstrap.svg" /> 

                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/mongodb.svg" />
                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/python.svg" />
                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/airflow.svg" />
                    <img v-if="index == 1" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/docker.svg" />
                    
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/mongodb.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/postgresql.svg" />
                    <img v-if="index == 2" class="md:h-8 md:w-8 h-5 w-5 rounded" src="./assets/logo/python.svg" />
                  </div>
                </card>
              </div>
            </div>
          </transition>
        </div>
      </div>
      <div class="flex items-center justify-center mt-5">
        <p class="font-bold font-xl">I apologize, this website is under construction.</p>
        <p class="font-bold font-xl">Thank you for your understanding.</p>
      </div>
      <div class="bg-footer">
        <div class="box-content">
          <transition name="slide" appear>
            <div class="side-content" v-if="toggleB">
              <div>Email : <a :href="'mailto:phetlada.tongkan@gmail.com'" @click="navigate" >phetlada.tongkan@gmail.com</a></div>
              <div>Github :<a href="https://github.com/Phetlada">https://github.com/Phetlada</a></div>
              <div>I'm looking for a new job. THANK YOU!</div>
            </div>
          </transition>
          </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.example[data-v-f3f3eg9] {
  color: red;
}
button {
  background-color: #303481;
  padding: 2%;
  border-radius: 10px;
  color: #f5f5f5;
}
button:hover {
  background-color: #608fbd;
  padding: 2%;
  border-radius: 10px;
  transform: scale(1.2) perspective(2px)
}
.slide-enter {
  opacity: 0;
}

.slide-enter-active {
  animation: slide-in 1s ease-in forwards;
  transition: opacity .5s;
}

.slide-leave-active {
  animation: slide-out 1s ease-out forwards;
  opacity: 0;
  transition: opacity 1s;
}


@keyframes slide-in {
  from {
    transform: translateY(20px);
  }

  to {
    transform: translateY(0);
  }
}

@keyframes slide-out {
  from {
    transform: translateY(0);
  }

  to {
    transform: translateY(20px);
  }
}
nav{
  position: sticky;
}
.bg-header {
  height: 500px;
  background-image: linear-gradient(#f5f5f5, #D6E6F2);
  margin-bottom: 15px;
}

.bg-footer {
  color: #222566;
  margin-top: 15px;
  height: auto;
  width: 100%;
  background-color: #D6E6F2;
}

.bg-content-work-experience {
  height: auto;
  width: 100%;
  background-color: #222566;
  /* background-image: linear-gradient(rgb(169, 193, 232), #f5f5f5); */
}

.bg-content-one {
  height: auto;
  margin-bottom: 15px;
  width: 100%;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-image: linear-gradient(rgb(255, 255, 255, 0.5), rgb(169, 193, 232)), url("assets/university.webp");
  /* background-color: #f5f5f5;  */
}

.side-content {
  width: 100%;
}

.box-content {
  padding-right: 3%;
  padding-left: 3%;
  padding-top: 1%;
  padding-bottom: 5%;
}

.big-font {
  font-weight: 500;
  font-size: 2.6rem;
}

header {
  line-height: 1.5;
}

h1,
p {
  color: #303481;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
.decs-topic{
  color: #f5f5f5;
  font-weight: 600;
  font-size: 1.7rem;
  padding-bottom: 1%;
}
.topic-content {
  position: relative;
  font-weight: 600;
  font-size: 2.2rem;
  padding-bottom: 1%;
  /* background-image: linear-gradient(rgb(255, 255, 255,0.2), rgba(194, 207, 228, 0.4)); */
}

.list-disc {
  height: 120px;
}

card {
  /* Add shadows to create the "card" effect */
  padding: 2%;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.3);
  transition: 0.3s;
  color: #303481;
  border-radius: 8px;
  background-color: #ffffff;
  opacity: 0.9;
  max-width: 100%;
}

.header-card {
  font-weight: 600;
  font-size: 1.7rem;
  padding-bottom: 10px;
}

.content-card {
  padding-top: 15px;
  font-weight: 400;
  font-size: 1.4rem;
}

.bottom-card {
  position: static;
  padding-top: 15px;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .topic-content {
    font-weight: 600;
    font-size: 2.5rem;
  }

  .box-content {
    padding-right: 3%;
    padding-left: 3%;
    padding-top: 1%;
    padding-bottom: 2%;
  }
}
</style>
