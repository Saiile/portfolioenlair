<script setup>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import About from "./components/About.vue";
import Projects from "./components/Projects.vue";
import Skills from "./components/Skills.vue";
import Formation from "./components/Formation.vue";
import Contact from "./components/Contact.vue";
</script>

<template>
  <div class="font-sans antialiased">
    <Navbar />
    <Home />
    <About />
    <Projects />
    <Skills />
    <Formation />
    <Contact />
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>
