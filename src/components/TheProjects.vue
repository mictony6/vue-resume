<script setup>
import ProjectItem from '@/components/ProjectItem.vue'
import projectLogo from '@/assets/static/images/projects.svg'
import oasisImg from '@/assets/static/images/oasis.png'
import artImg from '@/assets/static/images/art.png'
import snakeImg from '@/assets/static/images/snake.png'

const projects = [
  {
    title: 'Oasis',
    period: '2022-2023',
    link: 'https://github.com/mictony6/oasis-mern',
    description:
      'Web forum application for women experiencing violence. Communicate with other victims and seek out and book consultation with therapists. Developed with Express.js and React frameworks.',
    image: oasisImg
  },
  {
    title: '3D Art Portfolio',
    period: '2021',
    link: 'https://mictony.azurewebsites.net/',
    description:
      'Website made with Python Django for my 3d art portfolio where you can send requests for a commission or view a gallery of my sample works.',
    image: artImg
  },
  {
    title: 'Snake Game',
    period: '2021',
    link: 'https://github.com/mictony6/SnakeGame',
    description:
      'A snake-like game made with Java graphics library. Go thru five levels with different gimmicks and unique solutions.',
    image: snakeImg
  }
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
