<script setup>
</script>

<template>
    <div class="card greetings">
        <h1>Contact Me</h1>
        <div class="flex items-center justify-center">
            <svg class="h-4 w-4 text-yellow-500"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />  <polyline points="22,6 12,13 2,6" /></svg>
            <a href="mailto:phetlada.tongkan@gmail.com" class="p-1">phetlada.tongkan@gmail.com</a>
        </div>
       
    </div>
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

#spin {
  color: #303481;
  font-weight: 500;
}

#spin:after {
  content: "";
  font-weight: 500;
  animation: spin 5s linear infinite;
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
}

@keyframes spin {
  0% { content: "software deverloper"; }
  40% { content: "front-end deverloper"; }
  70% { content: "back-end deverloper"; }
  100% { content: "full-stack deverloper"; }
}
@media (min-width: 1024px) {
}
</style>
