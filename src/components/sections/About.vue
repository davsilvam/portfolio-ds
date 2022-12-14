<template>
  <section
    id="sobre_mim"
    class="w-full flex flex-col gap-8 py-8 px-11 md:px-36 bg-[url(@/assets/img/bg/mobile_stars.svg)] lg:bg-[url(@/assets/img/bg/stars.svg)] bg-center"
  >
    <h2
      class="flex items-center gap-4 text-neutral-100 text-2xl font-semibold"
      v-motion
      :initial="{ opacity: 0, x: -100 }"
      :enter="{ opacity: 1, x: 0 }"
      :delay="500"
    >
      <div class="h-6 w-1 bg-primary"></div>
      Sobre mim
    </h2>
    <div class="w-full flex flex-col items-center gap-6">
      <div
        class="w-full lg:w-2/5 flex flex-col items-center gap-4"
        v-motion-fade
        :delay="1000"
      >
        <img
          src="https://github.com/davsilvam.png"
          alt="Minha foto de perfil do Github"
          class="w-3/4 max-w-sm rounded-full border-4 border-primary"
        />
        <div class="flex flex-col items-center gap-1">
          <h3 class="text-primary text-2xl font-bold">David Silva</h3>
          <p class="text-neutral-300 text-sm font-semibold">
            Desenvolvedor Web
          </p>
        </div>
      </div>
      <div class="w-full lg:w-3/5 flex flex-col gap-4">
        <p class="text-neutral-100 text-justify" v-motion-fade :delay="1500">
          Oi, eu sou o <strong class="text-primary">David</strong> e atualmente
          estou na fase inicial dos meus estudos de
          <strong class="text-primary">Desenvolvimento Web</strong>,
          especificamente, a área
          <strong class="text-primary">Front-end</strong>. Eu estudo por conta
          própria, e quero alcançar grandes empresas, ou até mesmo, um projeto
          próprio com esse conhecimento.
        </p>
        <p class="text-neutral-100 text-justify" v-motion-fade :delay="2250">
          Adiante estão algumas das minhas
          <strong class="text-primary">redes sociais</strong>, além de um botão
          para baixar o meu <strong class="text-primary">currículo</strong>, te
          convido a explorá-los, ou se preferir, continue pela página e descubra
          mais um pouco sobre o meu
          <strong class="text-primary">perfil profissional</strong>.
        </p>
        <div class="flex items-center justify-center gap-4">
          <a
            href="https://github.com/davsilvam"
            target="_blank"
            class="flex items-center text-primary text-5xl"
            v-motion-slide-bottom
            :delay="500"
            ><i class="ri-github-fill"></i
          ></a>
          <a
            href="https://www.linkedin.com/in/davsilvam"
            target="_blank"
            class="flex items-center text-primary text-5xl"
            v-motion-slide-bottom
            :delay="500"
            ><i class="ri-linkedin-box-fill"></i
          ></a>
          <a
            href="https://drive.google.com/file/d/1QcnmglduxAO2EEgldALGCNqAOlTZUeIK/view?usp=sharing"
            class="flex items-center h-fit gap-2 px-4 py-2 border-2 text-primary border-primary rounded-lg font-semibold hover:bg-primary hover:text-white transition-colors duration-300"
            v-motion-fade
            :delay="1500"
          >
            Visualizar CV <i class="ri-download-2-line"></i>
          </a>
        </div>
        <div
          class="w-full flex items-center justify-center pt-10"
          v-motion-fade
          :delay="3000"
        >
          <a
            href="#habilidades"
            class="text-primary text-center font-semibold animate-pulse flex flex-col lg:flex-row lg:text-justify items-center lg:gap-6 text-lg"
          >
            Está pronto para saber um pouco sobre minhas habilidades?
            <i class="ri-arrow-down-s-line"></i>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
