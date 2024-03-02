<script setup>
import HeaderPostfolio from './components/HeaderPostfolio.vue';
import ContactMe from './components/ContactMe.vue';
</script>

<script>
export default {
  data() {
    return {
      toggleA: true,
      toggleB: true
    };
  }
}
</script>

<template>
  <div>
    <!-- Navigation Bar -->
    <nav class="flex-no-wrap fixed relative top-0 flex w-full items-center justify-between bg-[#FBFBFB] py-2 shadow-md shadow-black/5 dark:bg-gray-300 dark:shadow-gray/10 lg:flex-wrap lg:justify-start lg:py-4">
      <div class="mx-auto">
        <div class="flex items-center justify-between">
          <div>
            <h1 class="text-sm md:text-base">Phetlada</h1>
          </div>
          <div>
            <h1 class="text-sm md:text-base">Home | About | Resume | Projects</h1>
          </div>
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
          <h1 class="topic-content">Work Experience</h1>
          <div class="decs-topic text-xl">
            <span class="flex justify-between">
              <svg class="h-8 w-8 text-yellow-500" width="24" height="24" viewBox="0 0 24 24"
                stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" />
                <path d="M8 9l5 5v7h-5v-4m0 4h-5v-7l5 -5m1 1v-6a1 1 0 0 1 1 -1h10a1 1 0 0 1 1 1v17h-8" />
                <line x1="13" y1="7" x2="13" y2="7.01" />
                <line x1="17" y1="7" x2="17" y2="7.01" />
                <line x1="17" y1="11" x2="17" y2="11.01" />
                <line x1="17" y1="15" x2="17" y2="15.01" />
              </svg>
              | May. 2021 - Oct. 2021
            </span>
            Software Deverloper Internship
            <div class="text-lg">Creden Asia Co., Lid.</div>
          </div>
          <transition name="slide" appear>
            <div class="side-content" v-if="toggleB">
              <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <card>
                  <img src="./assets/landing-page.webp" />
                  <div class="content-card">
                    <span class="font-bold font-xl">Landing Page Development</span>
                    <ul class="list-disc ml-8 text-base">
                      <!-- <li>Build new landing pages based on business requirements.</li> -->
                      <li>Write clean and efficient HTML, CSS, and JavaScript code to create beautiful and user-friendly landing pages.</li>
                      <li>Collaborate with UI/UX designers to deliver landing pages that meet user needs.</li>
                    </ul>
                  </div>
                  <div class="bottom-card flex justify-end">
                    <button
                      class="align-middle select-none font-sans font-bold text-center uppercase"
                      type="button">
                      Read More
                    </button>
                  </div>
                </card>
                <card>
                  <img src="./assets/landing-page.webp" />
                  <div class="content-card">
                    <span class="font-bold font-xl">API Development</span>
                    <ul class="list-disc text-base ml-8">
                      <li>Design and build new APIs based on business requirements.</li>
                      <li>Write API code in a suitable language (e.g., Lua,Python,Node.js).</li>
                      <li>Create API documentation for developers.</li>
                    </ul>
                  </div>
                  <div class="bottom-card flex justify-end">
                    <button
                      class="align-middle select-none font-sans font-bold text-center uppercase"
                      type="button">
                      Read More
                    </button>
                  </div>
                </card>
                <card>
                  <img src="./assets/landing-page.webp" />
                  <div class="content-card">
                    <span class="font-bold font-xl">Developed a Back-Office Project</span>
                    <ul class="list-disc ml-8 text-base">
                      <li>Developed a back-office system to manage and organize data for a company.</li>
                      <li>The system was designed to be user-friendly and efficient, allowing users to easily manage their data.</li>
                    </ul>
                  </div>
                  <div class="bottom-card flex justify-end">
                    <button
                      class="align-middle select-none font-sans font-bold text-center uppercase"
                      type="button">
                      Read More
                    </button>
                  </div>
                </card>
              </div>
            </div>
          </transition>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
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

.bg-content-work-experience {
  height: auto;
  width: 100%;
  background-color: #D6E6F2;
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
  color: #303481;
  font-weight: 600;
  font-size: 1.7rem;
  padding-bottom: 1%;
}
.topic-content {
  position: relative;
  font-weight: 700;
  font-size: 2.6rem;
  padding-bottom: 1%;
  /* background-image: linear-gradient(rgb(255, 255, 255,0.2), rgba(194, 207, 228, 0.4)); */
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
  max-height: 500px;
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
