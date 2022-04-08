<script setup>
import ProjectItem from "@/components/ProjectItem.vue";
</script>

<template>
  <div class="projects">
    <h2>Take a look around what I've build</h2>
    <ProjectItem v-for="item in Array(10)" />
  </div>
</template>

<style scoped>
.projects {
  display: grid;
  grid-gap: 20px;
  grid-template-rows: 1fr;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
h2 {
  grid-column: 1 / -1;
  justify-self: center;
  font-size: 2rem;
  color: var(--primary);
  padding: 2rem;
  font-weight: bold;
}
</style>
