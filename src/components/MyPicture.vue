<script setup>
import picture from '@/assets/static/images/profile-pic.jpg'
</script>

<template>
  <figure class="image p-3">
    <img class="is-rounded" :src="picture" alt="my picture " />
  </figure>
</template>

<style scoped>
figure {
  border: solid var(--primary-alpha) 2px;
  box-shadow: 0 5px 0 var(--primary-alpha);
  height: 240px;
  aspect-ratio: 1/1;
  border-radius: 50%;
  overflow: hidden;
}
</style>
