<script setup>
  import { ref } from 'vue'
  import Header from './components/Header.vue'
  import Aside from './components/Aside.vue'
  import Main from './components/Main.vue'

  const asideState = ref(false)

  const toogleAside = (data) => (asideState.value = data)
</script>

<template>
  <div class="w-full flex flex-col">
    <Header :asideState="asideState" @asideState="toogleAside" />
    <Aside :asideState="asideState" @asideState="toogleAside" />
    <Main />
  </div>
</template>

<style scoped></style>
