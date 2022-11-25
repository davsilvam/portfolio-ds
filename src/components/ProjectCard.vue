<script setup>
  const props = defineProps([
    'title',
    'description',
    'image',
    'repository',
    'stacks',
  ])
</script>

<template>
  <a
    class="max-w-xs flex flex-col justify-start bg-neutral-800 rounded-xl cursor-pointer relative group border-2 border-primary hover:border-transparent"
    :href="repository"
    target="_blank"
  >
    <img class="rounded-t-xl" :src="`src/assets/img/${props.image}`" />
    <div class="flex flex-col py-5 px-6">
      <h2 class="text-lg font-bold text-primary">{{ props.title }}</h2>
      <div class="flex gap-2">
        <p
          class="flex items-center text-xs text-neutral-100 bg-primary px-2 py-0.5 rounded-xl font-semibold"
          v-for="stack in props.stacks"
          :key="stack.id"
        >
        #
          {{ stack.name }}
        </p>
      </div>
      <p class="text-neutral-300 text-sm text-justify pt-2">
        {{ props.description }}
      </p>
    </div>
    <div
      class="opacity-0 absolute w-full h-full flex group-hover:opacity-100 items-center justify-center bg-primary rounded-xl transition-all duration-300"
    >
      <h1 class="text-neutral-100 font-bold uppercase">Visualizar Projeto</h1>
    </div>
  </a>
</template>
