<script setup>
</script>

<template>
    <div class="greetings">
        <h1>Hello! I am</h1>
        <h3>
            Phetlada  Thongkarn
        </h3>
        <h3>I am a <span id="spin"></span></h3>
    </div>
</template>

<style scoped>
h3 {
    font-weight: 500;
    font-size: 2.6rem;
    position: relative;
    color: rgb(54, 53, 53);
}

h1 {
    font-weight: 500;
    font-size: 1.5rem;
    position: relative;
    color: rgb(54, 53, 53);
}
.greetings h3 {
    text-align: left;
    top: 100px;
}
.greetings h1 {
    text-align: left;
    top: 100px;
}

#spin {
  color: red;
}

#spin:after {
  content: "";
  animation: spin 5s linear infinite;
}

@keyframes spin {
  0% { content: "software deverloper"; }
  10% { content: "front-end deverloper"; }
  20% { content: "back-end deverloper"; }
  30% { content: "full-stack deverloper"; }
  40% { content: "software deverloper"; }
  50% { content: "front-end deverloper"; }
  60% { content: "back-end deverloper"; }
  70% { content: "full-stack deverloper"; }
  80% { content: "software deverloper"; }
  90% { content: "front-end deverloper"; }
  100% { content: "back-end deverloper"; }
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
}
</style>
