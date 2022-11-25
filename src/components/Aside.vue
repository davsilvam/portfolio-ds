<script setup>
  const props = defineProps(['asideState'])

  const emits = defineEmits(['asideState']) 

  const toogleAside = () => {
    emits('asideState', !props.asideState)
  }
</script>

<template>
  <aside
    class="lg:hidden w-20 h-screen flex items-center justify-center fixed top-0 z-10 bg-neutral-900 right-0 transition-transform duration-300 border-l-2 border-primary"
    :class="{ 'translate-x-full': !props.asideState }"
  >
    <button
      id="menu"
      class="lg:hidden text-primary hover:text-secondary text-xl fixed top-7"
      @click="toogleAside"
    >
      <i class="ri-menu-4-line"></i>
    </button>
    <ul
      class="flex flex-col items-start justify-center gap-3 text-primary font-semibold"
    >
      <li class="hover:text-neutral-900">
        <a
          href="#sobre_mim"
          class="flex py-3 px-4 bg-neutral-800 rounded-full hover:bg-primary"
        >
          <i class="ri-emotion-line"></i>
        </a>
      </li>
      <li class="hover:text-neutral-900">
        <a
          href="#habilidades"
          class="flex py-3 px-4 bg-neutral-800 rounded-full hover:bg-primary"
        >
          <i class="ri-code-line font-bold"></i>
        </a>
      </li>
      <li class="hover:text-neutral-900">
        <a
          href="#projetos"
          class="flex py-3 px-4 bg-neutral-800 rounded-full hover:bg-primary"
        >
          <i class="ri-layout-line"></i>
        </a>
      </li>
      <li class="hover:text-neutral-900">
        <a
          href="#contato"
          class="flex py-3 px-4 bg-neutral-800 rounded-full hover:bg-primary"
        >
          <i class="ri-question-answer-line"></i>
        </a>
      </li>
    </ul>
  </aside>
</template>
