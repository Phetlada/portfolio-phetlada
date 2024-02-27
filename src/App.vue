<script setup>
import HeaderPostfolio from './components/HeaderPostfolio.vue';
import ContactMe from './components/ContactMe.vue';
</script>

<script>
export default {
  data() {
    return {
      toggleA: true
    };
  }
}
</script>

<template>
  <div>
    <div class="bg-header">
      <!-- Navigation Bar -->
      <nav class="p-4">
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
      <div class="flex items-center justify-center">
        <HeaderPostfolio></HeaderPostfolio>
      </div>      
    </div>
    <!-- <div class="bg-contact-me flex items-center justify-center">
      <ContactMe></ContactMe>
    </div> -->
    <div class="bg-content-one flex items-center justify-center">
      <transition name="slide" appear>
          <div class="alert alert-info" v-if="toggleA">
              <div class="box-content">
                  <p class="text-wrap indent-8"><span class="big-font">I am</span> a software developer with over 2 years of experience building websites as designed, prioritizing clean code, and implementing user-friendly features.</p>       
              </div>
            </div>
      </transition>
    </div>
  </div>
</template>


<style scoped>
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
.bg-header{
  height: 500px;
  background-image: linear-gradient(#f5f5f5, #D6E6F2);
}
.bg-contact-me{
  height: auto;
  background-color: #D6E6F2;
  /* background-image: linear-gradient(#D6E6F2, #303481); */
}
.bg-content-one{
  height: auto;
  padding: 2%;
  background-color: #f5f5f5;
}
.box-content{
  max-width: 800px;
  font-weight: 500;
  font-size: 1.5rem;
}
.big-font{
  font-weight: 500;
  font-size: 2.6rem;
}

header {
  line-height: 1.5;
}

h1 , p{
  color: #303481;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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
}
</style>
