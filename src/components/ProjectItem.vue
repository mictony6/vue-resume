<script setup>
const props = defineProps(['title', 'description', 'period', 'link', 'image'])
</script>

<template>
  <a :href="props.link" target="_blank" class="is-flex">
    <div class="p-3">
      <figure class="image block">
        <img :src="props.image" alt="project-image" />
      </figure>
      <div class="content">
        <h4 class="title is-6">{{ props.title }}</h4>
        <p>{{ props.description }}</p>
        <small>{{ props.period }}</small>
      </div>
    </div>
  </a>
</template>

<style scoped>
p,
small {
  font-size: 0.9rem;
}
a {
  text-decoration: none;
  color: initial;
}
a > div {
  border: rgba(0, 0, 0, 0.25) dashed 1px;
  transition: transform 0.1s;
  transition-timing-function: cubic-bezier(0.38, 0.15, 0, 1.23);
}

a > div:hover {
  background: linear-gradient(var(--gradient));
  border-color: transparent;
  transform: scale(102%) rotate(2deg);
}

a:nth-child(even) > div:hover {
  transform: scale(102%) rotate(-2deg);
}

img {
  object-fit: cover;
  border: solid 5px white;
  height: 120px;
}
</style>
