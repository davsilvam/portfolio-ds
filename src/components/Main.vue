<script setup>
  import About from './sections/About.vue'
  import Skills from './sections/Skills.vue'
  import Projects from './sections/Projects.vue'
  import Contact from './sections/Contact.vue'
  import Footer from './Footer.vue'
  import Divisor from './Divisor.vue'

  import waves from '@/assets/img/bg/waves.svg'
  import mobileWaves from '@/assets/img/bg/mobile_waves.svg'
  import peaks from '@/assets/img/bg/peaks_b.svg'
  import peaksB from '@/assets/img/bg/peaks.svg'
  import footer from '@/assets/img/bg/footer.svg'
</script>

<template>
  <main class="w-full flex flex-col bg-neutral-900 pt-24">
    <About />
    <Divisor class="hidden lg:block" :src="waves" />
    <Divisor class="lg:hidden" :src="mobileWaves" />
    <Skills />
    <Divisor :src="peaks" />
    <Projects />
    <Divisor :src="peaksB" />
    <Contact />
    <Divisor :src="footer" />
    <Footer />
  </main>
</template>
