<script setup>
import TheAbout from '@/components/TheAbout.vue'
import TheProjects from '@/components/TheProjects.vue'
import TheNavigation from '@/components/TheNavigation.vue'
import TheContact from '@/components/TheContact.vue'
import TheSkills from '@/components/TheSkills.vue'
import MyPicture from '@/components/MyPicture.vue'
import TheEducation from '@/components/TheEducation.vue'
import { ref } from 'vue'

let prevTarget = ref(null)
function handleScroll(target) {
  target.scrollIntoView()
  if (prevTarget.value) {
    prevTarget.value.classList.remove('section-focused')
  }
  setTimeout(() => {
    target.classList.add('section-focused')
  }, 120)
  prevTarget.value = target
}
</script>

<template>
  <header class="is-sticky-top has-background-white">
    <div class="wrapper">
      <nav>
        <TheNavigation @scrollTo="(refName) => handleScroll(this.$refs[refName].$el)" />
      </nav>
    </div>
  </header>

  <main class="wrapper columns my-2">
    <div class="column is-one-quarter-desktop is-one-third">
      <div class="is-flex is-flex-direction-column">
        <MyPicture />
        <TheSkills ref="skills" />
        <TheEducation ref="education" />
        <TheContact ref="contact" />
      </div>
    </div>
    <div class="column">
      <TheAbout ref="about" />
      <TheProjects ref="projects" />
    </div>
  </main>
</template>
