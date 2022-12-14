<script setup>
  import { ref } from 'vue'

  const asideState = ref(false)

  const toogleAside = () => {
    asideState.value = !asideState.value
  }
</script>

<template>
  <button
    id="menu"
    class="z-20 fixed top-7 right-6 lg:hidden text-xl text-primary hover:text-secondary"
    @click="toogleAside"
  >
    <i class="ri-menu-4-line"></i>
  </button>
  <aside
    class="fixed top-0 right-0 lg:hidden w-44 h-screen flex items-center justify-center z-10 translate-x-0 bg-neutral-900 border-l-2 border-primary transition-transform duration-300"
    :class="{ 'translate-x-full': !asideState }"
  >
    <ul
      class="flex flex-col items-start justify-center gap-6 text-primary font-semibold"
    >
      <li>
        <a href="#sobre_mim">Sobre mim</a>
      </li>
      <li>
        <a href="#habilidades">Habilidades</a>
      </li>
      <li>
        <a href="#projetos">Projetos</a>
      </li>
      <li>
        <a href="#contato">Contato</a>
      </li>
    </ul>
  </aside>
</template>
