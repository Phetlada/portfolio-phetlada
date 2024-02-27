<script setup>
import ContactMe from './ContactMe.vue';
</script>

<template>
    <div class="greetings">
        <h1>Hello! I am</h1>
        <h3>
            Phetlada  Thongkarn
        </h3>
        <h2><span id="spin"></span></h2>
        <div class="position-under">
            <ContactMe></ContactMe>   
        </div>
        
    </div>
</template>

<style scoped>
h3 {
    font-weight: 500;
    font-size: 2.6rem;
    position: relative;
    color: #303481;
}

h2 {
    font-weight: 400;
    font-size: 2.0rem;
    position: relative;
    color: #303481;
}

h1 {
    font-weight: 500;
    font-size: 1.5rem;
    position: relative;
    color: #9fc5e1;
}
.position-under{
    position: relative;
    top: 170px;
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

#spin {
  color: #303481;
  font-weight: 500;
}

#spin:after {
  content: "";
  font-weight: 500;
  animation: spin 5s linear infinite;
}

@keyframes spin {
  0% { content: "software deverloper"; }
  40% { content: "front-end deverloper"; }
  70% { content: "back-end deverloper"; }
  100% { content: "full-stack deverloper"; }
}
@media (min-width: 1024px) {
    .greetings h3 {
        text-align: center;
        top: 150px;
    }
    .greetings h1 {
        text-align: center;
        top: 150px;
    }
    .greetings h2 {
    text-align: center;
    top: 150px;
    .position-under{
    position: relative;
    top: 180px;
}
}
}
</style>
