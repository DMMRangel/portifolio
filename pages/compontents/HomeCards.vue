<script setup>

const cards = [
  {
    title: 'Quem sou',
    description: 'Desenvolvedor Full Stack com mais de 3 anos de experiência criando aplicações web modernas, escaláveis e responsivas. Apaixonado por tecnologia e boas práticas de desenvolvimento.',
    icon: "fluent-emoji:man-beard-light"
  },
  {
    title: 'Minha especialidade',
    description: 'Atuo no front-end e back-end, dominando frameworks como Vue.js, React, Next.js e NestJS. Tenho forte foco em performance, reutilização de componentes e integrações com APIs.',
    icon: ""
  },
  {
    title: 'Experiência Recente',
    description: 'Participei de projetos em empresas de tecnologia, desenvolvendo dashboards, integrações e sistemas completos. Trabalhei com equipes ágeis e processos SCRUM/Kanban.',
    icon: ""
  },
  {
    title: 'Stack Técnica',
    description: 'Front-end: Vue.js, React, Next.js\nBack-end: NestJS, .NET, Prisma\nOutros: Tailwind, Docker, Git, Figma',
    icon: ""
  },
  {
    title: 'Formação e Aprendizado Contínuo',
    description: 'Tecnólogo em Desenvolvimento Web (2023) e certificações em React, Node.js e Vue.js. Estou sempre evoluindo minhas habilidades e acompanhando tendências do mercado.',
    icon: ""
  },
  {
    title: 'Idiomas',
    description: 'Inglês avançado, capaz de ler documentação técnica e comunicar ideias em projetos internacionais.',
    icon: ""
  }
]

</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
    <div
      v-for="(card, index) in cards"
      :key="index"
      class="bg-lime-950 p-4 rounded-lg shadow-md"
    >
      <!-- <h3 class="font-bold text-lg">{{ card.title }}</h3> -->
      <p class="text-gray-400 font-semibold">{{ card.description }}</p>
    </div>
  </div>
</template>
