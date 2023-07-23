<script setup>
const skills = ['Javascript', 'Java', 'C#', 'C', 'Python', 'DBS']
</script>

<template>
  <section id="skills" class="content">
    <h3 class="title is-5">Skills</h3>
    <div v-for="(skill, index) in skills" :key="index" class="skill-item p-3 m-1 is-inline-block">
      {{ skill }}
    </div>
  </section>
</template>

<style scoped>
.skill-item {
  max-width: min-content;
  background: var(--secondary);
  font-family: var(--font-mono);
  border: solid 1px white;
  background: var(--primary-alpha);
}

.skill-item:hover {
  transform: scale(102%) rotate(2deg);
  border: dashed 1px var(--primary);
  background: white;
}

.skill-item:nth-child(even):hover {
  transform: scale(102%) rotate(-2deg);
}
</style>
