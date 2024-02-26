<script setup>
import HeaderPostfolio from './components/HeaderPostfolio.vue';
</script>

<template>
  <div>
    <div class="bg-header">
      <!-- Navigation Bar -->
      <nav class="bg-gray-800/40 text-white p-4">
        <div class="container mx-auto">
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
  </div>
</template>

<style scoped>
.bg-header{
  height: 500px;
  background-color: rgb(255, 255, 255);
}

header {
  line-height: 1.5;
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
