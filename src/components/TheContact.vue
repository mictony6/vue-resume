<script setup>
import instagramIcon from '@/assets/static/images/instagram.svg'
import facebookIcon from '@/assets/static/images/facebook.svg'
import githubIcon from '@/assets/static/images/github.svg'
import linkedinIcon from '@/assets/static/images/linkedin.svg'
</script>

<template>
  <section id="contact" class="content">
    <h3 class="title is-5">Currently Available</h3>
    <p><a href="mailto:michaelanthonybitoon@gmail.com">michaelanthonybitoon@gmail.com</a></p>
    <p><a href="tel:+639667780755">+639667780755</a></p>
    <div id="social-links" class="is-flex is-align-items-center">
      <span class="icon">
        <img
          data-link="https://www.instagram.com/mictony06/"
          :src="instagramIcon"
          alt="instagram link"
        />
      </span>
      <span class="icon">
        <img
          data-link="https://www.facebook.com/mictony6"
          :src="facebookIcon"
          alt="facebook link"
        />
      </span>
      <span class="icon">
        <img data-link="https://github.com/mictony6" :src="githubIcon" alt="github link" />
      </span>
      <span class="icon">
        <img
          data-link="https://www.linkedin.com/in/michael-anthony-bitoon-7b43a0273/"
          :src="linkedinIcon"
          alt="linkedin link"
        />
      </span>
    </div>
  </section>
</template>

<style scoped>
.icon {
  margin-inline-end: 15px;
  border: 1px solid white;
  cursor: pointer;
}

.icon:hover {
  transform: scale(102%) rotate(2deg);
  border: dashed 1px var(--primary);
  background: var(--secondary);
}

.icon:nth-child(even):hover {
  transform: scale(102%) rotate(-2deg);
}
</style>
