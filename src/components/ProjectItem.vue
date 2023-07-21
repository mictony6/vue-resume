<script setup>
const props = defineProps(['title', 'description', 'period', 'link', 'image'])
</script>

<template>
  <a :href="props.link" target="_blank">
    <figure class="image">
      <img :src="props.image" alt="project-image" class="m-auto" />
    </figure>
    <h4 class="title is-6">{{ props.title }}</h4>
    <div class="content">
      <p>{{ props.description }}</p>
      <small>{{ props.period }}</small>
    </div>
  </a>
</template>

<style scoped>
a {
  text-decoration: none;
  color: initial;
}

img {
  object-fit: cover;
  border: solid 5px white;
  max-width: 240px;
  max-height: 120px;
}
</style>
