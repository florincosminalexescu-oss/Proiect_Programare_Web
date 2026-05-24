<script setup>
import Education from './components/Education.vue';
import Experince from './components/Experience.vue';
import Footer from './components/Footer.vue';
import Hero from './components/Hero.vue';
import NavBar from './components/NavBar.vue'
import Projects from './components/Projects.vue';
</script>

<template>
  <NavBar> </NavBar>
  <Hero> </Hero>

  <Projects id="projects">  </Projects>

  <Experience id="experience"> </Experience>
  <Education id="education"> </Education>

  <Footer>  </Footer>




</template>



<style >
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap');



* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'DM Sans', sans-serif;
  background-color: #f7f6f4;
}




</style>