<script setup>
import { ref } from 'vue'

let menuShow = ref(false)
function handleBurger() {
  menuShow.value = !menuShow.value
}
</script>

<template>
  <nav class="navbar">
    <div class="navbar-brand">
      <a id="logo" href="/" class="navbar-item">M</a>

      <a
        @click.prevent="handleBurger"
        role="button"
        :class="[menuShow ? 'is-active' : '', 'navbar-burger']"
        aria-label="menu"
        aria-expanded="false"
        data-target="navMenu"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div id="navMenu" :class="[menuShow ? 'is-active' : '', 'navbar-menu']">
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
  color: black;
  background: var(--secondary);
  transform: scale(102%) rotate(2deg);
}
a:nth-child(even):hover {
  transform: scale(102%) rotate(-2deg);
}
a.navbar-item:focus {
  background: var(--secondary);
  color: unset;
}
#logo {
  width: 64px;
  aspect-ratio: 1/1;
  margin: 0;
  padding: 0;
  font-size: 3rem;
  text-align: center;
  font-family: var(--font-mono);
}

.navbar,
.navbar-menu {
  background: transparent !important;
}
</style>
