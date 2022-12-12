<template>
  <section
    id="contato"
    class="w-full flex flex-col gap-8 py-8 bg-primary px-11 md:px-36"
  >
    <h2
      class="flex items-center gap-4 text-neutral-100 text-2xl font-semibold"
      v-motion
      :initial="{ opacity: 0, x: -100 }"
      :visibleOnce="{ opacity: 1, x: 0 }"
      :delay="1000"
    >
      <div class="h-6 w-1 bg-neutral-900"></div>
      <span class="flex gap-2">
        Contato
        <i class="ri-question-answer-line font-normal"></i>
      </span>
    </h2>
    <div class="w-full flex items-center justify-center">
      <p
        class="w-fit text-neutral-100 font-medium mb-8 rounded-lg flex items-center justify-center gap-4 px-8 py-4 bg-neutral-900 text-justify"
        v-motion
        :initial="{ opacity: 0 }"
        :visibleOnce="{ opacity: 1 }"
        :delay="500"
      >
        <i class="ri-chat-3-line text-xl"></i>
        Caso tenha se interessado no meu perfil e/ou no meu trabalho, você pode
        me contatar:
      </p>
    </div>
    <div
      class="w-full flex flex-wrap lg:flex-nowrap justify-between gap-10 text-center"
      v-motion-slide-visible-once-left
      :delay="2000"
    >
      <a
        href="https://www.linkedin.com/in/davsilvam"
        target="_blank"
        class="w-full lg:w-1/2 bg-neutral-800 py-6 px-8 rounded-md relative cursor-pointer hover:bg-neutral-900 transition-colors duration-300"
      >
        <h2 class="text-xl font-bold text-primary">Linkedin</h2>
        <p class="text-neutral-200 text-sm">
          Mandando uma mensagem para meu perfil no Linkedin.
        </p>
        <i
          class="ri-linkedin-fill absolute text-3xl -top-5 -left-5 text-primary py-2 px-3 bg-neutral-900 rounded-full"
        ></i>
      </a>
      <a
        href="mailto:contatodavidmai@gmail.com"
        class="w-full lg:w-1/2 bg-neutral-800 py-6 px-8 rounded-md relative cursor-pointer hover:bg-neutral-900 transition-colors duration-300"
      >
        <h2 class="text-xl font-bold text-primary">Email</h2>
        <p class="text-neutral-200 text-sm">
          Enviando um email para mim, pelo: <br />
          <strong class="text-primary">contatodavidmaia@gmail.com</strong>
        </p>
        <i
          class="ri-mail-line absolute text-3xl -top-5 -right-5 text-primary py-2 px-3 bg-neutral-900 rounded-full"
        ></i>
      </a>
    </div>
  </section>
</template>
