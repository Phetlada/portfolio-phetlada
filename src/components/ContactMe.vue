<script setup>
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
  <transition name="slide" appear>
    <div class="alert alert-info" v-if="toggleA">
      <a class="card greetings flex items-center justify-center" :href="'mailto:phetlada.tongkan@gmail.com'" @click="navigate">
          <div class="flex items-center justify-center">
              <svg class="h-5 w-5 text-yellow-500"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />  <polyline points="22,6 12,13 2,6" /></svg>
              <h1 class="ml-2">Contact Me</h1>
          </div>
        </a>
    </div>
  </transition>
</template>

<style scoped>
h3 {
    font-weight: 500;
    font-size: 2rem;
    color: #303481;
}

h2 {
    font-weight: 400;
    font-size: 1.2rem;
}

h1 {
    font-weight: 500;
    font-size: 1.2rem;
}
.greetings h3 {
    text-align: center;
    top: 120px;
}
.greetings h2 {
    text-align: center;
    top: 120px;
}
.greetings h1 {
    text-align: center;
    top: 120px;
}

.card {
  /* Add shadows to create the "card" effect */
  padding: 2%;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  color: #D6E6F2;
  border-radius: 20px;
  background-color: #303481;
  opacity: 0.9;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
  background-color: #608fbd;
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

@media (min-width: 1024px) {
}
</style>
