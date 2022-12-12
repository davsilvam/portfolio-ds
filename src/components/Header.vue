<template>
  <header
    class="w-full flex justify-between items-center bg-neutral-800 px-11 py-6 md:px-20 fixed z-10"
  >
    <img
      src="@/assets/img/logo_ds.png"
      alt="Logo com o nome David em uma fonte manuscrita e uma pequena ilustração de um gatinho siamês desenhado."
      class="w-[30%] max-w-[120px] h-fit"
    />
    <nav class="relative">
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
        <a
          href="https://drive.google.com/file/d/1QcnmglduxAO2EEgldALGCNqAOlTZUeIK/view?usp=sharing"
          class="flex gap-2 px-4 py-2 border-2 font-semibold border-primary rounded-lg hover:bg-primary hover:text-white transition-colors duration-300"
        >
          Visualizar CV
          <i class="ri-download-2-line"></i>
        </a>
      </ul>
    </nav>
  </header>
</template>
