<template>
  <NavBar/>
  <HeroSection/>
</template>

<script>
import NavBar from './components/Navbar.vue';
import HeroSection from './components/Hero.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    HeroSection,
}
}
</script>

<style>
  :root {
    --primary-color: #000;
    --secondary-color: #fff;
    --light-color: #e8e8e8;
  }
  body {
    font-family: 'Montserrat', sans-serif;
    line-height: 1.7;
  }
  .btn:active, .btn:focus {
    box-shadow: none !important;
    outline: none !important;
  }
  .btn-action {
        background-color: var(--secondary-color);
        color: var(--primary-color);
        border-color: var(--secondary-color);
  }
  .btn-action:hover, .btn-action:focus {
        background-color: var(--secondary-color);
        color: var(--primary-color);
        border-color: var(--secondary-color);
  }
</style>
