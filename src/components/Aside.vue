<script setup>
  const props = defineProps(['asideState'])

  const emits = defineEmits(['asideState'])

  const toogleAside = () => {
    emits('asideState', !props.asideState)
  }
</script>

<template>
  <aside
    class="fixed top-0 right-0 lg:hidden w-44 h-screen flex items-center justify-center z-10 bg-neutral-900 border-l-2 border-primary"
    :class="{ 'right-full': !props.asideState }"
  >
    <button
      id="menu"
      class="lg:hidden text-primary hover:text-secondary text-xl fixed top-7 right-6"
      @click="toogleAside"
    >
      <i class="ri-menu-4-line"></i>
    </button>
    <ul
      class="flex flex-col items-start justify-center gap-6 text-primary font-semibold"
    >
      <li class="flex gap-2">
        <i class="ri-emotion-line font-normal"></i>
        <a href="#sobre_mim"> Sobre mim </a>
      </li>
      <li class="flex gap-2">
        <i class="ri-code-line"></i>
        <a href="#habilidades"> Habilidades </a>
      </li>
      <li class="flex gap-2">
        <i class="ri-layout-line font-normal"></i>
        <a href="#projetos"> Projetos </a>
      </li>
      <li class="flex gap-2">
        <i class="ri-question-answer-line font-normal"></i>
        <a href="#contato"> Contato </a>
      </li>
    </ul>
  </aside>
</template>
