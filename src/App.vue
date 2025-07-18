<script setup>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Rockets from './components/Rockets.vue';
import Testimonials from './components/Testimonials.vue';
import Contact from './components/Contact.vue';
</script>

<template>
  <Navbar />
  <main class="max-w-4xl mx-auto scroll-smooth">
        <section id="hero" class="flex flex-col-reverse justify-center sm:flex-row p-6 items-center gap-8 mb-12 w-full h-screen">
             <Hero />
        </section>
        <section id="rockets" class="p-6 my-12">
              <Rockets />
        </section>
        <section id="testimonials" class="p-6 my-12 scroll-mt-20">
            <Testimonials />
        </section>
         <section id="contact" class="p-6 my-12 scroll-m-16">
                <Contact />
         </section>
  </main>
  <footer id="footer" class="bg-teal-700 text-white text-xl">
        <section class="max-w-4xl mx-auto p-4 flex flex-col sm:flex-row sm:justify-between">
            <address>
                <h2>Acme Rocket-Powered Products, Inc.</h2>
                555 Astro Way<br>
                Fairfield, New Jersey 12345-5555<br>
                Email: <a href="mailto:inquiries@acmerockets.com">inquiries@AcmeRockets.com</a><br>
                Phone: <a href="tel:+15555555555">(555) 555-5555</a>
            </address>
            <nav class="hidden md:flex flex-col gap-2" aria-label="footer">
                <a href="#rockets" class="hover:opacity-90">Our Rockets</a>
                <a href="#testimonials" class="hover:opacity-90">Testimonials</a>
                <a href="#contact" class="hover:opacity-90">Contact Us</a>
            </nav>
            <div class="flex flex-col sm:gap-2 scroll-m-10">
                <p class="text-right">Copyright&copy; <span id="year">2025</span></p>
                <p class="text-right">All Rights Reserved</p>
            </div>
        </section>
  </footer> 
</template>

