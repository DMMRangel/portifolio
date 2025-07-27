<script setup lang="ts">
import { ref } from 'vue'

const activeSection = ref<string | null>('inicio')

const setActiveSection = (section: string) => {
  console.log(section);
  if (section != null) {
    console.log("if section");
    activeSection.value = section;
  }
}

const items = ref([
  {
    label: 'English',
    value: 'english',
  },
  {
    label: 'Português',
    value: 'portuguese',
  }
])
</script>

<template>
  <header id="inicio">
    <nav class="flex
      justify-center
      p-4
      fixed top-0 right-0 left-0"
      aria-label="Global"
    >
      <div class="
        flex px-4 py-2 gap-6
        rounded-full
        shadow-sm shadow-green-500/50
        inset-shadow-indigo-500/50
        bg-background/80
        backdrop-blur-[3px]
      ">
        <UButton
          tag="a"
          href="#inicio"
          color="neutral"
          variant="link"
          class="cursor-pointer"
          :class="{ 'text-primary font-bold': activeSection === 'inicio' }"
          @click="setActiveSection('inicio')"
        >
          # Início
        </UButton>
        <UButton
          tag="a"
          href="#trabalhos"
          color="neutral"
          variant="link"
          class="cursor-pointer"
          :class="{ 'text-primary font-bold': activeSection === 'trabalhos' }"
          @click="setActiveSection('trabalhos')"
        >
          # Trabalhos
        </UButton>
        <UButton
          tag="a"
          href="#curriculo"
          color="neutral"
          variant="link"
          class="cursor-pointer"
          :class="{ 'text-primary font-bold': activeSection === 'curriculo' }"
          @click="setActiveSection('curriculo')"
        >
          # Currículo
        </UButton>
        <UButton
          tag="a"
          href="#contato"
          color="neutral"
          variant="link"
          class="cursor-pointer"
          :class="{ 'text-primary font-bold': activeSection === 'contato' }"
          @click="setActiveSection('contato')"
        >
          # Contato
        </UButton>
        <UButton
          tag="a"
          target="_blank"
          href="https://github.com/DMMRangel"
          color="neutral"
          variant="link"
          class="cursor-pointer"
          :class="{ 'text-primary font-bold': activeSection === 'github' }"
          @click="setActiveSection('github')"
        >
          # GitHub
        </UButton>
        <UDropdownMenu
          :items="items"
          :ui="{
            content: 'w-fit'
          }"
        >
          <UButton icon="i-lucide:languages" size="xl" color="primary" variant="link"  class="cursor-pointer"/>
        </UDropdownMenu>
      </div>
    </nav>
  </header>

  <main class="flex flex-col gap-8 max-w-6xl mx-auto">
    <section class="flex flex-col items-center gap-8 mb-8 mt-25">
      <NuxtImg
        src="https://github.com/DMMRangel.png"
        width="200"
        class="rounded-full"
      />
      <h1 class="tracking-tight font-bold text-pretty text-3xl sm:text-4xl lg:text-5xl text-shadow-md text-center max-w-5xl mx-auto">
        Olá, eu sou <span class="text-success">Daniel Rangel</span><br>desenvolvedor Full Stack
      </h1>
      <h2 class="text-2xl">Seja bem-vindo ao meu portifólio!</h2>
      <div class="flex gap-8 items-center">
        <Icon name="devicon:vuejs" class="text-success" size="42" />
        <Icon name="devicon:react" class="text-success" size="42" />
        <Icon name="devicon:dotnetcore" class="text-success" size="42" />
        <Icon name="devicon:nestjs" class="text-success" size="42" />
        <Icon name="devicon:javascript" class="text-success" size="42" />
        <Icon name="devicon:csharp" class="text-success" size="42" />
      </div>
    </section>
    <section class="flex justify-center">
      <p class="tracking-tight text-pretty text-xl text-shadow-lg px-6 max-w-3xl text-justify">
        Sou desenvolvedor com mais de 3 anos de experiência, focado em criar interfaces modernas, performáticas e acessíveis. Tenho visão de produto, boa comunicação com times multidisciplinares e participação ativa em rotinas ágeis. Busco sempre escrever código limpo e escalável, e estou em constante evolução, pronto para encarar novos desafios e contribuir com soluções de impacto!
      </p>
    </section>
    <section>
      <h3
        id="trabalhos"
        class="text-2xl font-bold"
        :class="{ 'text-primary font-bold': activeSection === 'trabalhos' }"
      ># Trabalhos</h3>
      <p class="text-muted">Aqui estão alguns dos meus trabalhos mais recentes.</p>
      <div class="h-[25vh]"></div>
    </section>

    <section>
      <h3
        id="curriculo"
        class="text-2xl font-bold"
        :class="{ 'text-primary font-bold': activeSection === 'curriculo' }"
      ># Currículo</h3>
      <p class="text-muted">Saque meu currículo aí vá.</p>
      <div class="h-[25vh]"></div>
    </section>

    <section>
      <h3
        id="contato"
        class="text-2xl font-bold"
        :class="{ 'text-primary font-bold': activeSection === 'contato' }"
      ># Contato</h3>
      <p class="text-muted">Entre em contato comigo através das redes sociais.</p>
            <div class="flex gap-8 items-center">
        <Icon name="devicon:vuejs" class="text-success" size="42" />
        <Icon name="devicon:react" class="text-success" size="42" />
        <Icon name="devicon:dotnetcore" class="text-success" size="42" />
        <Icon name="devicon:nestjs" class="text-success" size="42" />
        <Icon name="devicon:javascript" class="text-success" size="42" />
        <Icon name="devicon:csharp" class="text-success" size="42" />
      </div>
      <div class="h-[25vh]"></div>
    </section>
  </main>

</template>