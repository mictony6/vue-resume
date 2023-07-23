<script setup>
const skills = ['Javascript', 'Java', 'C#', 'C', 'Python', 'DBS']
</script>

<template>
  <section id="skills">
    <h3>Skills</h3>
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
}
</style>
