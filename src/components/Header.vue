<script setup>
  import { ArrowDownTrayIcon } from '@heroicons/vue/24/solid'
</script>

<template>
  <header
    class="fixed z-10 w-full flex items-center justify-between px-11 py-6 md:px-20 bg-neutral-800"
  >
    <img
      src="@/assets/img/logo_ds.png"
      alt="Logo com o nome David em uma fonte manuscrita e uma pequena ilustração de um gatinho siamês desenhado."
      class="h-fit w-[30%] max-w-[120px]"
    />
    <nav class="flex items-center pl-[80px]">
      <ul class="hidden lg:flex items-center gap-8 text-primary">
        <li class="hover:text-secondary font-semibold">
          <a href="#sobre_mim">Sobre mim</a>
        </li>
        <li class="hover:text-secondary font-semibold">
          <a href="#habilidades">Habilidades</a>
        </li>
        <li class="hover:text-secondary font-semibold">
          <a href="#projetos">Projetos</a>
        </li>
        <li class="hover:text-secondary font-semibold">
          <a href="#contato">Contato</a>
        </li>
      </ul>
    </nav>
    <div class="w-[30%] max-w-[200px] flex items-center justify-center">
      <a
        href="https://drive.google.com/file/d/1QcnmglduxAO2EEgldALGCNqAOlTZUeIK/view?usp=sharing"
        class="hidden lg:flex gap-2 px-4 py-2 border-2 text-sm text-primary font-semibold border-primary rounded-lg hover:bg-primary hover:text-white transition-colors duration-300"
      >
        Visualizar CV
        <ArrowDownTrayIcon class="w-5" />
      </a>
    </div>
  </header>
</template>
