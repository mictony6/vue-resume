<script setup>
import { RouterView } from 'vue-router'
import TheNavigation from '@/components/TheNavigation.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav class="container">
        <TheNavigation />
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped></style>
