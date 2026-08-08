<script setup lang="ts">

import Navbar from './components/layout/Navbar.vue'
import Footer from './components/layout/Footer.vue'
import HeroSection from './components/HeroSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'

if (localStorage.getItem('theme') === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    document.documentElement.classList.add('dark');
  } else {
    document.documentElement.classList.remove('dark');
  }


</script>




<template>
  <Navbar />

   <HeroSection />
  
  <ExperienceSection />
  <SkillsSection />
  <ProjectsSection />
  <ContactSection />

  <Footer />
</template>

<style scoped></style>
