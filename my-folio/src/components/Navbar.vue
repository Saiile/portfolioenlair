<template>
<nav class="fixed top-4 left-0 right-0 z-50 transition-all duration-300 px-8">

    <div
      class="hidden md:block max-w-md mx-auto bg-black backdrop-blur-lg shadow-lg rounded-full px-4 py-2"
    >
      <div class="flex items-center justify-center space-x-7">
        <a href="#home" class="Isenheim text-white hover:text-gray-300 transition-colors duration-300 font-medium">Accueil</a>
        <a href="#about" class="Isenheim text-white hover:text-gray-300 transition-colors duration-300 font-medium">À Propos</a>
        <a href="#projects" class="Isenheim text-white hover:text-gray-300 transition-colors duration-300 font-medium">Projets</a>
        <a href="#skills" class="Isenheim text-white hover:text-gray-300 transition-colors duration-300 font-medium">Skills</a>
        <a href="#contact" class="Isenheim text-white hover:text-gray-300 transition-colors duration-300 font-medium">Contact</a>
      </div>
    </div>

    <div class="md:hidden flex justify-end">
      <button
        @click="toggleMenu"
        class="w-12 h-12 bg-black backdrop-blur-lg shadow-lg rounded-lg flex items-center justify-center text-white focus:outline-none transition-all duration-300 hover:scale-110 z-50 relative"
      >
        <img
          v-if="!isMenuOpen"
          :src="menuIcon"
          alt="openMenu"
          class="w-6 h-6"
        />
        <img
          v-else
          :src="crossIcon"
          alt="closeMenu"
          class="w-6 h-6"
        />
      </button>
    </div>

    <div
      v-if="isMenuOpen"
      class="md:hidden fixed inset-0 bg-black z-40 flex items-center justify-center"
    >
      <div class="flex flex-col items-center space-y-6">
        <a href="#home" class="Isenheim text-white font-medium text-xl" @click="closeMenu">Accueil</a>
        <a href="#about" class="Isenheim text-white font-medium text-xl" @click="closeMenu">À Propos</a>
        <a href="#projects" class="Isenheim text-white font-medium text-xl" @click="closeMenu">Projets</a>
        <a href="#skills" class="Isenheim text-white font-medium text-xl" @click="closeMenu">Skills</a>
        <a href="#contact" class="Isenheim text-white font-medium text-xl" @click="closeMenu">Contact</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";
import menuIcon from "../assets/menu.png";
import crossIcon from "../assets/cross.png";

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};
</script>

<style scoped>
@font-face {
  font-family: "isenheim";
  src: url("../assets/font/Isenheim.otf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

.Isenheim {
  font-family: "isenheim", sans-serif;
}
</style>
