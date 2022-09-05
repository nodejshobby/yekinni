<template>
  <div data-bs-spy="scroll" data-bs-target="#scrollNavbar" data-bs-offset="0" tabindex="0">
    <NavBar/>
    <HeroSection/>
    <AboutSection/>
    <ProjectSection/>
    <SkillSection/>
    <ContactSection/>
    <FooterSection/>
  </div>
</template>

<script>
import NavBar from './components/Navbar.vue';
import HeroSection from './components/Hero.vue';
import AboutSection from './components/About.vue';
import ProjectSection from './components/Project.vue';
import SkillSection from './components/Skills.vue';
import ContactSection from './components/Contact.vue';
import FooterSection from './components/Footer.vue';
import AOS from 'aos';

export default {
  name: 'App',
  components: {
    NavBar,
    HeroSection,
    AboutSection,
    ProjectSection,
    SkillSection,
    ContactSection,
    FooterSection,
  },
  mounted(){
    AOS.init()
  }
}
</script>

<style>
  :root {
    --primary-color: #01064b;
    --secondary-color: #fff;
    --light-color: #e8e8e8;
    --dark-blue: #01011d;
    --light-blue: #3884f7;
  }
  
  html,body {
    margin: 0;
    padding: 0;
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

  .blue-hover-effect:focus, .blue-hover-effect:active {
    background-color: var(--primary-color);
  }

  .blue-hover-effect:hover {
    background-color: var(--primary-color);
  }
</style>
