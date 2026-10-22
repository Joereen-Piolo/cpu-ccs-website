<script setup>
import { navItems, programs, departments, partners } from './data/ccsData.js'

import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import ProgramsSection from './components/ProgramsSection.vue'
import FacultySection from './components/FacultySection.vue'
import PartnershipsSection from './components/PartnershipsSection.vue'
</script>

<template>
  <div class="app">
    <Navbar :navItems="navItems" />
    <HeroSection />
    <ProgramsSection :programs="programs" />
    <FacultySection :departments="departments" />
    <PartnershipsSection :partners="partners" />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>