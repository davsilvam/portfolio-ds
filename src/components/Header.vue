<script setup>
  import { ref } from 'vue'

  const props = defineProps(['asideState'])
  const emits = defineEmits(['asideState'])

  const toogleAside = () => {
    emits('asideState', !props.asideState)
  }
</script>

<template>
  <header class="w-full flex justify-between items-center bg-neutral-800 px-11 py-6 md:px-20 fixed z-10">
    <img
      src="@/assets/img/logo_ds.png"
      alt="Logo com o nome David em uma fonte manuscrita e uma pequena ilustração de um gatinho siamês desenhado."
      class="w-[30%] max-w-[120px] h-fit"
    />
    <nav class="relative">
      <ul class="hidden lg:flex items-center gap-8 text-primary">
        <li class="hover:text-secondary font-semibold"><a href="#sobre_mim">Sobre mim</a></li>
        <li class="hover:text-secondary font-semibold"><a href="#habilidades">Habilidades</a></li>
        <li class="hover:text-secondary font-semibold"><a href="#projetos">Projetos</a></li>
        <li class="hover:text-secondary font-semibold"><a href="#contato">Contato</a></li>
        <button class="flex gap-2 px-4 py-2 border-2 font-semibold border-primary rounded-lg hover:bg-primary hover:text-white transition-colors duration-300">
          Baixar CV 
          <i class="ri-download-2-line"></i></button>
      </ul>

      <button id="menu" class="lg:hidden text-primary hover:text-secondary text-xl fixed top-7" @click="toogleAside">
        <i class="ri-menu-4-line"></i>
      </button>
    </nav>
  </header>
</template>