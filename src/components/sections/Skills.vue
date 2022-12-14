<script setup>
  import { ref } from 'vue'

  const skillTitle = ref('Que mergulho, ein?')
  const skillSubtitle = ref('Boas-vindas à seção de habilidades.')
  const skillMessage = ref(
    'Selecione a habilidade para ver sua descrição e como trabalho com elas!'
  )

  const skills = ref([
    {
      icon: 'devicon-html5-plain',
      name: 'HTML',
      subtitle: 'HyperText Markup Language',
      description:
        'Domino a sintaxe, tags semânticas, formulários, links internos e externos, meta, acessibilidade. Uso-o para a construção de páginas estáticas para a Web.',
    },
    {
      icon: 'devicon-css3-plain',
      name: 'CSS',
      subtitle: 'Cascading Style Sheets',
      description:
        'Domino o CSS Layout, Box Model, Displays, Grid e Flex, Media Queries, Animações CSS. Essas folhas de estilo são a base para a estilização dos meus sites.',
    },
    {
      icon: 'devicon-javascript-plain',
      name: 'JS',
      subtitle: 'JavaScript',
      description:
        'Domino estrutura e tipos de dados, Loops, condicionais, operadores, seletores, manipulação de DOM, Functions, ES6, arrays e métodos, funções assíncronas. Este é responsável pela lógica e dinamismo do site, formando a tríade do Desenvolvimento Web.',
    },
    {
      icon: 'devicon-sass-original',
      name: 'Sass',
      subtitle: 'Syntactically Awesome Style Sheets',
      description:
        'Domino a sintaxe do SCSS, variáveis, aninhamento, módulos, Mixins. Adoro trabalhar com o aninhamento do SCSS, além de segmentar os estilos das minhas páginas em vários documentos, facilitando o código e a revisão.',
    },
    {
      icon: 'devicon-tailwindcss-plain',
      name: 'Tailwind CSS',
      subtitle: 'Framework CSS com classes predefinidas',
      description:
        'Domino a sintaxe, Breakpoints, Box Model, dimensões, cores, tipografia, extensões do tema. Me apaixonei pela simplicidade do Tailwind, gosto muito de trabalhar com sua biblioteca de cores e suas classes utilitárias.',
    },
    {
      icon: 'devicon-vuejs-plain',
      name: 'Vue.js',
      subtitle: 'Framework JavaScript Progressivo',
      description:
        'Domino diretivas, propriedades computadas, observadores, Life Cycle Hooks, slots, props e emits, rotas, gerenciamento de estado (Pinia), composition API, componentes, reatividade. O Vue é o framework em que estou focando meus projetos.',
    },
  ])

  const showStack = (stack) => {
    skillTitle.value = skills.value[stack].name
    skillSubtitle.value = skills.value[stack].subtitle
    skillMessage.value = skills.value[stack].description
  }
</script>

<template>
  <section
    id="habilidades"
    class="w-full flex flex-col justify-center gap-8 py-24 px-11 md:px-36 bg-primary"
  >
    <h2
      class="flex items-center gap-4 text-neutral-100 text-2xl font-semibold"
      v-motion
      :initial="{ opacity: 0, x: -100 }"
      :visibleOnce="{ opacity: 1, x: 0 }"
      :delay="500"
    >
      <div class="h-6 w-1 bg-neutral-900"></div>
      Habilidades
    </h2>
    <div
      class="flex items-center justify-center w-full lg:min-h-72"
      v-motion
      :initial="{ opacity: 0, x: -100 }"
      :visibleOnce="{ opacity: 1, x: 0 }"
      :delay="500"
    >
      <div
        class="flex flex-col justify-center items-center lg:flex-row gap-8 w-full lg:w-4/5 lg:gap-10"
      >
        <div class="lg:w-1/2">
          <h2 class="text-3xl font-bold text-neutral-900">
            {{ skillTitle }}
          </h2>
          <h3 class="text-neutral-800 pb-2 text-lg font-semibold">
            {{ skillSubtitle }}
          </h3>
          <p class="text-neutral-100 text-justify">
            {{ skillMessage }}
          </p>
        </div>
        <div
          class="lg:w-1/2 grid grid-cols-3 gap-6 lg:gap-4 place-items-center"
        >
          <div
            class="flex items-center text-4xl text-primary bg-neutral-800 w-fit p-4 rounded-full border-2 border-transparent hover:border-neutral-900 hover:text-neutral-900 hover:bg-primary cursor-pointer transition-colors duration-200"
            v-for="skill in skills"
            :key="skill.id"
            @click="showStack(skills.indexOf(skill))"
            @mouseenter="showStack(skills.indexOf(skill))"
          >
            <i :class="skill.icon"></i>
          </div>
        </div>
      </div>
    </div>
    <div
      class="w-full flex items-center justify-center pt-20"
      v-motion
      :initial="{ opacity: 0 }"
      :visibleOnce="{ opacity: 1 }"
      :delay="1500"
    >
      <a
        href="#projetos"
        class="text-neutral-900 text-center font-semibold animate-pulse flex flex-col lg:flex-row lg:text-justify items-center justify-center lg:gap-6 text-lg lg:w-3/5"
      >
        Indo mais fundo, você encontrará muitos tesouros: meus projetos.
        <i class="ri-arrow-down-s-line"></i>
      </a>
    </div>
  </section>
</template>
