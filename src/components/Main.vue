<script setup>
  import About from './sections/About.vue'
  import Skills from './sections/Skills.vue'
  import Projects from './sections/Projects.vue'
  import Contact from './sections/Contact.vue'
  import Footer from './Footer.vue'
  import Divisor from './Divisor.vue'
</script>

<template>
  <main class="w-full flex flex-col bg-neutral-900 pt-24">
    <About />
    <Divisor class="hidden lg:block" :src="'src/assets/img/bg/waves.svg'" />
    <Divisor class="lg:hidden" :src="'src/assets/img/bg/mobile_waves.svg'" />
    <Skills />
    <Divisor :src="'src/assets/img/bg/peaks_b.svg'" />
    <Projects />
    <Divisor :src="'src/assets/img/bg/peaks.svg'" />
    <Contact />
    <Divisor :src="'src/assets/img/bg/footer.svg'" />
    <Footer />
  </main>
</template>
