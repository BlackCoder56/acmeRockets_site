<script>
    const initApp = () => {

    }
</script>
<template>
    <header class="bg-teal-700 text-white sticky top-0 z-10">
        <section class="max-w-4xl mx-auto p-4 flex justify-between items-center">
            <h1 class="text-3xl font-medium">
            <a href="#hero">
                🚀 Ace Rockets
            </a>
            </h1>
            <div>
                <button id="hamburger-button" class="text-3xl md:hidden cursor-pointer">
                    &#9776;
                </button>
                <nav class="hidden sm:block space-x-8 text-xl" aria-label="main">
                    <a href="#rockets" class="hover:opacity-90">Our Rockets</a>
                    <a href="#testimonials" class="hover:opacity-90">Testimonials</a>
                    <a href="#contact" class="hover:opacity-90">Contact Us</a>
                </nav>
            </div>
        </section>        
        <section id="mobile-menu" class="absolute top-0 bg-black w-full text-5x flex-col justify-content-center origin-top animate-open-menu hidden">
            <button class="text-8xl self-end px-6">
                &times;
            </button>
            <nav class="flex flex-col min-h-screen items-center py-8" aria-label="mobile">
                <a href="#hero" class="w-full text-center py-6 hover:opacity-90">Home</a>
                <a href="#rockets" class="w-full text-center py-6 hover:opacity-90">Our Rockets</a>
                <a href="#testimonials" class="w-full text-center py-6 hover:opacity-90">Testimonials</a>
                <a href="#contact" class="w-full text-center py-6 hover:opacity-90">Contact Us</a>
                <a href="#footer" class="w-full text-center py-6 hover:opacity-90">Legal</a>
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

    .animate-open-menu {
    animation: open-menu 0.5s ease-in-out forwards;
    transform-origin: top;
    }
</style>