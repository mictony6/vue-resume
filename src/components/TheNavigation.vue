<script setup>
// import { ref } from 'vue'
//
// window.addEventListener('scroll', handleScroll)
// let prevScrollPos = window.scrollY
// let navShow = ref(true)
// let nav = ref(null)
// function handleScroll(e) {
//   let currentScrollPos = window.scrollY
//   // makes nav bar go out of page when scrolling down
//   navShow.value = prevScrollPos >= currentScrollPos
//   prevScrollPos = currentScrollPos
// }
</script>

<template>
  <nav class="navbar">
    <div class="navbar-brand">
      <a id="logo" href="/" class="navbar-item is-128x128">M</a>
    </div>
    <div class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item" @click.prevent="$emit('scrollTo', 'about')" href="/">ABOUT</a>
        <a class="navbar-item" @click.prevent="$emit('scrollTo', 'skills')" href="#">SKILLS</a>
        <a class="navbar-item" @click.prevent="$emit('scrollTo', 'projects')" href="#"
          >PROJECTS & CONTRIBUTION</a
        >
        <a class="navbar-item" @click.prevent="$emit('scrollTo', 'education')" href="#"
          >EDUCATION</a
        >
        <a class="navbar-item" @click.prevent="$emit('scrollTo', 'contact')" href="#">CONTACT</a>
      </div>
    </div>
  </nav>
</template>

<style scoped>
a:hover {
  background: white;
  background: var(--secondary);
  transform: scale(102%) rotate(2deg);
}
a:nth-child(even):hover {
  transform: scale(102%) rotate(-2deg);
}

#logo {
  width: 64px;
  aspect-ratio: 1/1;
  margin: 0;
  font-size: 4rem;
  text-align: center;
  font-family: var(--font-mono);
  color: var(--primary);
}
</style>
