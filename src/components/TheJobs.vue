<script setup>
import resumeFile from '@/assets/static/files/michaelresume.pdf'
import fileIcon from '@/assets/static/images/file-pdf.svg'
</script>

<template>
  <section id = "job" class="content">
    <div class="is-flex">
    <span class="icon mr-2">
        <img :src="fileIcon" alt="projects-icon" class="mr-auto"/>
    </span>
      <a :href="resumeFile">Download Full Resume</a>
    </div>
    <h3 class="title is-5">Job History</h3>
    <div class="job-item">
      <h4 class="subtitle is-6">DTE Endurance Asia (Itemhound Corp.)</h4>
      <small>Fullstack Web Development Intern — 2023</small>
    </div>
    <div class="job-item mb-2">
      <h4 class="subtitle is-6">UP Venture Media</h4>
      <small>Freelance SEO Content Writer — 2024-2026</small>
    </div>
  </section>
</template>

<style scoped></style>