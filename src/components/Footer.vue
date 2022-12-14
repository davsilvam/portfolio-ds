<script setup>
  const year = new Date().getFullYear()
</script>

<template>
  <footer
    class="w-full flex justify-between pt-8 lg:pt-0 items-center px-11 md:px-36 pb-8"
  >
    <h3 class="text-primary font-semibold">David Silva | &copy; {{ year }}</h3>
    <div class="flex gap-4 items-center">
      <a
        href="https://www.linkedin.com/in/davsilvam"
        target="_blank"
        class="text-primary text-2xl"
      >
        <i class="ri-linkedin-fill"></i>
      </a>
      <a
        href="https://github.com/davsilvam"
        target="_blank"
        class="text-primary text-2xl"
      >
        <i class="ri-github-line"></i>
      </a>
    </div>
  </footer>
</template>
