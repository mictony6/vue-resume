<script setup>
import TheAbout from '@/components/TheAbout.vue'
import TheProjects from '@/components/TheProjects.vue'
import TheSide from '@/components/TheSide.vue'
</script>

<template>
  <main class="container columns m-auto">
    <div class="column is-one-fifth-desktop is-flex">
      <TheSide />
    </div>
    <div class="column">
      <TheAbout />
      <TheProjects />
    </div>
  </main>
</template>
