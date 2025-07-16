<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Rockets from './components/Rockets.vue';
</script>

<template>
  <Navbar />
  <main class="max-w-4xl mx-auto">
        <Hero />
        <Rockets />
  </main>
  <!-- <h1 class="text-5xl font-bold underline text-slate-800">
    Hello world!
  </h1> -->
</template>

