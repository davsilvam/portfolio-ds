<script setup>
  import { ref } from 'vue'

  import ProjectCard from '../ProjectCard.vue'
  import wintermanSrc from '@/assets/img/winterman_sc.png'
  import linkpackSrc from '@/assets/img/linkpack_sc.png'
  import towoSrc from '@/assets/img/towo_sc.png'
  import rocketpaySrc from '@/assets/img/rocketpay_sc.png'
  import twentyOneSrc from '@/assets/img/21_dias_de_codigo_sc.png'
  import parsiSrc from '@/assets/img/parsi_sc.png'

  const projects = ref([
    {
      title: 'Winterman',
      description:
        'O Winterman se baseia em um página que traz o clima da cidade que o usuário pesquisar.',
      repository: 'https://github.com/davsilvam/winterman-app',
      image: wintermanSrc,
      stacks: [{ name: 'Tailwind' }, { name: 'Vue.js' }],
      delay: 500,
    },
    {
      title: 'Link Pack',
      description:
        'O Link Pack é um projeto cujo objetivo é agregar os links das minhas redes sociais e portfólio.',
      repository: 'https://github.com/davsilvam/link-pack',
      image: linkpackSrc,
      stacks: [{ name: 'Tailwind' }, { name: 'Vue.js' }],
      delay: 800,
    },
    {
      title: 'ToWo List',
      description:
        'A ToWo List auxilia o registro de suas atividades física que envolvam séries de exercícios.',
      repository: 'https://github.com/davsilvam/spirited-away',
      image: towoSrc,
      stacks: [
        { name: 'Tailwind' },
        { name: 'Vue.js' },
        { name: 'TypeScript' },
      ],
      delay: 1100,
    },
    {
      title: 'Rocketpay',
      description:
        'O Rocketpay é um componente que simula o formulário de preenchimento de cartão de crédito.',
      repository: 'https://github.com/davsilvam/explorer-lab',
      image: rocketpaySrc,
      stacks: [{ name: 'JavaScript' }],
    },
    {
      title: '21 Dias de Códigos',
      description:
        'Este é um desafio proposto pela Rocketseat no qual em 21 dias serão realizados projetos diários.',
      repository: 'https://github.com/davsilvam/21-dias-de-codigo',
      image: twentyOneSrc,
      stacks: [{ name: 'HTML' }, { name: 'CSS' }, { name: 'JavaScript' }],
      delay: 1400,
    },
    {
      title: 'Parsi (desenvolvendo...)',
      description:
        'A Parsi ajuda a registrar suas transações, auxiliando no melhor gerenciamento dos gastos.',
      repository: 'https://github.com/davsilvam/parsi-app',
      image: parsiSrc,
      stacks: [{ name: 'CSS' }, { name: 'Vue.js' }, { name: 'Firebase' }],
      delay: 1700,
    },
  ])
</script>

<template>
  <section id="projetos" class="w-full flex flex-col gap-8 py-8">
    <h2
      class="flex items-center gap-4 text-neutral-100 text-2xl font-semibold px-11 md:px-36"
      v-motion
      :initial="{ opacity: 0, x: -100 }"
      :visibleOnce="{ opacity: 1, x: 0 }"
      :delay="500"
    >
      <div class="h-6 w-1 bg-primary"></div>
      Projetos
    </h2>
    <div
      class="w-full flex items-center justify-center"
      v-motion
      :initial="{ opacity: 0 }"
      :visibleOnce="{ opacity: 1 }"
      :delay="300"
    >
      <p
        class="lg:w-3/5 text-neutral-100 font-medium mb-8 rounded-lg flex items-center gap-4 px-8 py-4 bg-primary text-justify mx-11 md:mx-36"
      >
        <i class="ri-lightbulb-line text-xl"></i>
        Você chegou ao museu das bolhas! Em algumas, há repositórios para alguns
        dos meus projetos, clique sobre elas e conseguirá ver sua documentação
        no GitHub.
      </p>
    </div>
    <div
      class="w-full grid lg:grid-cols-2 xl:grid-cols-3 justify-center place-items-center gap-4 gap-y-10 bg-[url('/src/assets/img/bg/mobile_bubbles.svg')] lg:bg-[url('/src/assets/img/bg/bubbles.svg')] bg-contain px-11 md:px-36"
    >
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :image="project.image"
        :repository="project.repository"
        :stacks="project.stacks"
        v-motion
        :initial="{ opacity: 0 }"
        :visibleOnce="{ opacity: 1 }"
        :delay="project.delay"
      >
      </ProjectCard>
    </div>
    <div class="flex flex-col gap-12 justify-center items-center mt-4 lg:mt-8">
      <a
        href="https://github.com/davsilvam?tab=repositories"
        target="_blank"
        class="border-2 border-primary text-primary py-2 px-8 rounded-md hover:text-neutral-100 hover:bg-primary font-semibold transition-colors duration-300 flex items-center justify-center gap-1"
        v-motion-pop-visible-once
        :delay="800"
        >Confira mais projetos <i class="ri-add-line text-xl"></i
      ></a>
      <a
        href="#contato"
        class="text-primary text-center font-semibold animate-pulse flex flex-col lg:flex-row lg:text-justify items-center lg:gap-6 text-lg"
        v-motion
        :initial="{ opacity: 0 }"
        :visibleOnce="{ opacity: 1 }"
        :delay="1500"
      >
        Chegou a hora de chamar ajuda.
        <i class="ri-arrow-down-s-line"></i>
      </a>
    </div>
  </section>
</template>
