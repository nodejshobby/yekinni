<template>
  <NavBar/>
  <HeroSection/>
  <AboutSection/>
  <ProjectSection/>
</template>

<script>
import NavBar from './components/Navbar.vue';
import HeroSection from './components/Hero.vue';
import AboutSection from './components/About.vue';
import ProjectSection from './components/Project.vue';



export default {
  name: 'App',
  components: {
    NavBar,
    HeroSection,
    AboutSection,
    ProjectSection
  }
}
</script>

<style>
  :root {
    --primary-color: #000328;
    --secondary-color: #fff;
    --light-color: #e8e8e8;
    --dark-blue: #000112;
  }

  html,body {
    margin: 0;
    padding: 0;
    width: 100%;
    overflow-x: hidden;
  }

  body {
    font-family: 'Montserrat', sans-serif;
    line-height: 1.7;
    color: var(--dark-blue);
    margin-top: 4.2rem;
  }

  .btn:active, .btn:focus {
    box-shadow: none !important;
    outline: none !important;
  }
  .btn-action {
        background-color: var(--secondary-color);
        color: var(--dark-blue);
        border-color: var(--secondary-color);
        font-weight: 500;
  }
  .btn-action:hover, .btn-action:focus {
        background-color: var(--secondary-color);
        color: var(--primary-color);
        border-color: var(--secondary-color);
  }
  .section-padding {
    padding: 3rem 0;
  }
  .blue-hover-effect {
    border-color: var(--dark-blue);
    font-weight: 600;
  }
  .blue-hover-effect:hover {
    background-color: var(--primary-color);
  }
</style>
