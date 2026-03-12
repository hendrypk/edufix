<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Problems from './components/Problems.vue'
import Services from './components/Services.vue'
import Steps from './components/Steps.vue'
import CTA from './components/CTA.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="antialiased scroll-smooth">
    <Navbar />
    <Hero />
    <Problems />
    <Services />
    <Steps />
    <CTA />
    <Footer />
  </div>
</template>

<style>
body { background: #ffffff; font-family: 'Inter', sans-serif; }
</style>