<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)
const isClosing = ref(false)

const toggleMenu = () => {
  if (isMenuOpen.value) {
    // If open, trigger closing animation
    isClosing.value = true
    setTimeout(() => {
      isMenuOpen.value = false
      isClosing.value = false
    }, 400) // match the close-menu animation duration
  } else {
    isMenuOpen.value = true
  }
}
</script>


<template>
  <header class="bg-teal-700 text-white sticky top-0 z-10">
    <section class="max-w-4xl mx-auto p-4 flex justify-between items-center">
      <h1 class="text-3xl font-medium">
        <a href="#hero">🚀 Ace Rockets</a>
      </h1>

      <div>
        <!-- Hamburger button -->
        <button @click="toggleMenu" 
  :class="{ 'toggle-btn': isMenuOpen }"  class="text-3xl md:hidden cursor-pointer relative w-8 h-8">
          <!-- &#9776; -->
          <div class="bg-white w-8 h-1 rounded absolute top-5 -mt-0.5 transition-all duration-500
          before:content-[''] before:bg-white before:w-8 before:h-1 before:rounded before:absolute before:-translate-x-4 before:-translate-y-2.5 before:transition-all before:duration-500
          after:content-[''] after:bg-white after:w-8 after:h-1 after:rounded after:absolute after:-translate-x-4 after:translate-y-2.5 after:transition-all after:duration-500"></div>
        </button>

        <!-- Desktop nav -->
        <nav class="hidden md:block space-x-8 text-xl" aria-label="main">
          <a href="#rockets" class="hover:opacity-90">Our Rockets</a>
          <a href="#testimonials" class="hover:opacity-90">Testimonials</a>
          <a href="#contact" class="hover:opacity-90">Contact Us</a>
        </nav>
      </div>
    </section>

    <!-- Mobile Menu -->
    <section
      v-show="isMenuOpen || isClosing"
  :class="[isClosing ? 'animate-close-menu' : 'animate-open-menu']"
      class="absolute top-68 bg-black w-full text-white text-5xl flex flex-col justify-center origin-top animate-open-menu"
    >
      <!-- <button @click="toggleMenu" class="text-8xl self-end px-6">
        &times;
      </button> -->
      <nav class="flex flex-col min-h-screen items-center py-8" aria-label="mobile">
        <a href="#hero" class="w-full text-center py-6 hover:opacity-90" @click="toggleMenu">Home</a>
        <a href="#rockets" class="w-full text-center py-6 hover:opacity-90" @click="toggleMenu">Our Rockets</a>
        <a href="#testimonials" class="w-full text-center py-6 hover:opacity-90" @click="toggleMenu">Testimonials</a>
        <a href="#contact" class="w-full text-center py-6 hover:opacity-90" @click="toggleMenu">Contact Us</a>
        <a href="#footer" class="w-full text-center py-6 hover:opacity-90" @click="toggleMenu">Legal</a>
      </nav>
    </section>
  </header>
</template>

<style scoped>
@keyframes open-menu {
  0% {
    transform: scaleY(0);
  }
  8% {
    transform: scaleY(1.2);
  }
  100% {
    transform: scaleY(1);
  }
}

@keyframes close-menu {
  0% {
    transform: scaleY(1);
  }
  100% {
    transform: scaleY(0);
  }
}

.animate-open-menu {
  animation: open-menu 0.5s ease-in-out forwards;
  transform-origin: top;
}

.animate-close-menu {
  animation: close-menu 0.4s ease-in-out forwards;
  transform-origin: top;
}

</style>
