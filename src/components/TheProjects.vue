<script setup>
import ProjectItem from '@/components/ProjectItem.vue'
import projectLogo from '@/assets/static/images/projects.svg'
import oasisImg from '@/assets/static/images/oasis.png'
import artImg from '@/assets/static/images/art.png'
import snakeImg from '@/assets/static/images/snake.png'
import dalogicImg from '@/assets/static/images/dalogic.png'
import taylorBook from '@/assets/static/images/taylorbook.png'
import chichaImg from '@/assets/static/images/chicha.png'
import soonGame from '@/assets/static/images/soon.png'

const projects = [
  {
    title: 'Run, Chicha! Run!',
    period: '2024',
    link: 'https://github.com/mictony6/chicharun',
    description:
      'A rouge-lite adventure game where you play as cyborg pig who aims to take rid the Earch of the evil aliens. This is a solid and simple game with a fun and replayable game loop, made using Unity Engine.',
    image: chichaImg,
  },
  {
    title: 'Oasis',
    period: '2022-2023',
    link: 'https://github.com/mictony6/oasis-mern',
    description:
      'Web forum application for women experiencing violence. Communicate with other victims and seek out and book consultation with therapists. Developed with Express.js and React frameworks.',
    image: oasisImg,
  },
  {
    title: 'Dalogic',
    period: '2024',
    link:'https://mictony6.itch.io/dalogic-game',
    description: "A digi-board game inspired by Damath, but with a binary twist! You can play alone with a bot, or with other people using the multiplayer matchmaking. Made with Javascript.",
    image: dalogicImg,
  },

  {
    title: '3D Art Portfolio',
    period: '2021',
    link: 'https://mictony.azurewebsites.net/',
    description:
      'Website made with Python Django for my 3d art portfolio where you can send requests for a commission or view a gallery of my sample works.',
    image: artImg,
  },
    {
    title: 'Taylor Swift Fan Book',
    period: '2024',
    link: 'https://www.amazon.com/125-Facts-About-Taylor-Swift/dp/B0D2J9255B',
    description:'Designed and illustrated a commercial fan-made book for the pop stars community and fans. Had fun making this as a Swiftie myself. Designs were created inside figma and ported to Adobe InDesign.',
    image: taylorBook,
  },
    {
    title: 'Cracks',
    period: '2026',
    link: 'https://github.com/mictony6/digging-game',
    description:
      'An upcoming post-apocalyptic horror mining game. One of the bigger projects Ive been undertaking since 2025.',
    image: soonGame,
  },
  {
    title: 'Snake Game',
    period: '2021',
    link: 'https://github.com/mictony6/SnakeGame',
    description:
      'A snake-like game made with Java graphics library. Go thru five levels with different gimmicks and unique solutions.',
    image: snakeImg,
  },


]
</script>

<template>
  <section id="projects" class="mt-4">
    <header class="is-flex is-justify-content-space-between is-align-items-center my-5">
      <h3 class="title is-5 is-flex is-align-items-center my-auto">
        <span class="icon mr-2">
          <img :src="projectLogo" alt="projects-icon" />
        </span>
        Projects
      </h3>
      <a target="_blank" href="https://github.com/mictony6" class="ml-auto"
        >View Github Repositories -></a
      >
    </header>
    <div class="columns is-variable is-2 is-multiline">
      <ProjectItem
        class="column is-one-third-desktop is-half-tablet is-full-mobile"
        v-bind="project"
        v-for="(project, index) in projects"
        :key="index"
      />
    </div>
  </section>
</template>

<style scoped></style>
