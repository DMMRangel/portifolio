<script setup>

const cards = [
  // {
  //   title: 'Quem sou',
  //   description: 'Desenvolvedor Full Stack com mais de 4 anos de experiência criando aplicações web modernas, escaláveis e responsivas. Apaixonado por tecnologia e boas práticas de desenvolvimento.',
  //   icon: "fluent-emoji:man-beard-light"
  // },
  {
    title: 'Quem sou',
    description: 'Desenvolvedor Full Stack com mais de 4 anos de experiência criando aplicações web modernas, escaláveis e responsivas.',
    icon: "hugeicons:developer"
  },
  // {
  //   title: 'Minha especialidade',
  //   description: 'Atuo no front-end e back-end, dominando frameworks como Vue.js, React, Next.js e NestJS. Tenho forte foco em performance, reutilização de componentes e integrações com APIs.',
  //   icon: ""
  // },
  {
    title: 'Minha especialidade',
    description: 'Atuo no front-end e back-end, dominando frameworks como Vue.js, React, Next.js e .NET.',
    icon: "meteor-icons:devices"
  },
  // {
  //   title: 'Experiência Recente',
  //   description: 'Participei de projetos em empresas de tecnologia, desenvolvendo dashboards, integrações e sistemas completos. Trabalhei com equipes ágeis e processos SCRUM/Kanban.',
  //   icon: ""
  // },
  {
    title: 'Experiência Recente',
    description: 'Participei de projetos de tecnologia, desenvolvendo dashboards, integrações e sistemas completos.',
    icon: "fluent:people-team-24-regular"
  },
  {
    title: 'Stack Técnica',
    description: 'Front-end: Vue.js, React, Next.js\nBack-end: NestJS, .NET, Prisma\nOutros: Tailwind, Docker, Git, Figma',
    icon: "maki:charging-station"
  },
  // {
  //   title: 'Formação e Aprendizado Contínuo',
  //   description: 'Tecnólogo em Desenvolvimento Web (2023) e certificações em React, Node.js e Vue.js. Estou sempre evoluindo minhas habilidades e acompanhando tendências do mercado.',
  //   icon: ""
  // },
  {
    title: 'Formação e Aprendizado Contínuo',
    description: 'Tecnólogo em Desenvolvimento Web (2023) e certificações em React, Node.js e Vue.js.',
    icon: "maki:college"
  },
  // {
  //   title: 'Idiomas',
  //   description: 'Inglês avançado, capaz de ler documentação técnica e comunicar ideias em projetos internacionais.',
  //   icon: ""
  // }
  {
    title: 'Idiomas',
    description: 'Inglês avançado, habituado com documentação técnica e comunicação de ideias em projetos internacionais.',
    icon: "mingcute:translate-2-ai-line"
  }
]

</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
    <div
      v-for="(card, index) in cards"
      :key="index"
      class="flex items-center p-4 rounded-lg shadow-md gap-4 bg-lime-950"
    >
      <!-- <h3 class="font-bold text-lg">{{ card.title }}</h3> -->
      <Icon :name="card.icon" class="text-success flex-none" size="42" />
      <p class="text-gray-300 ">{{ card.description }}</p>
    </div>
    <!-- <UCard variant="outline" v-for="(card, index) in cards" :key="index" class="p-4 rounded-lg shadow-md gap-4 bg-lime-950" as="div">
      <template #header>
        <h3 class="font-bold text-lg">{{ card.title }}</h3>
      </template>

      <Icon :name="card.icon" class="text-success flex-none" size="42" />
      <p class="text-gray-300 ">{{ card.description }}</p>
    </UCard> -->
  </div>
</template>
