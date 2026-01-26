<script setup>
import TheAbout from '@/components/TheAbout.vue'
import TheProjects from '@/components/TheProjects.vue'
import TheNavigation from '@/components/TheNavigation.vue'
import TheContact from '@/components/TheContact.vue'
import TheSkills from '@/components/TheSkills.vue'
import MyPicture from '@/components/MyPicture.vue'
import TheEducation from '@/components/TheEducation.vue'
import TheJobs from '../components/TheJobs.vue'
import { ref } from 'vue'
import { onMounted, onUnmounted } from 'vue'

// highlights target element
let prevTarget = ref(null)
function handleNavigation(target) {
  target.scrollIntoView()
  if (prevTarget.value) {
    prevTarget.value.classList.remove('section-focused')
  }
  setTimeout(() => {
    target.classList.add('section-focused')
  }, 120)
  prevTarget.value = target
}

let prevScrollPos = window.scrollY
let navShow = ref(true)
let navNormal = ref(true)
let nav = ref(null)
function handleScroll() {
  let currentScrollPos = window.scrollY
  // changes navbar style when at top
  navNormal.value = currentScrollPos <= nav.value.offsetHeight
  // makes nav bar go out of page when scrolling down
  navShow.value = prevScrollPos >= currentScrollPos
  prevScrollPos = currentScrollPos
}
onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
// window.addEventListener('scroll', handleScroll)
</script>

<template>
  <header
    ref="nav"
    class="is-sticky-top"
    :class="[navNormal ? 'nav-normal' : navShow ? 'nav-active' : 'nav-hidden']"
  >
    <div class="wrapper">
      <nav>
        <TheNavigation @scrollTo="(refName) => handleNavigation(this.$refs[refName].$el)" />
      </nav>
    </div>
  </header>

  <main class="wrapper columns my-2">
    <div class="column is-one-quarter-desktop is-one-third">
      <div class="is-flex is-flex-direction-column">
        <MyPicture />
        <TheSkills ref="skills" />
        <TheJobs ref="jobs"/>
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
