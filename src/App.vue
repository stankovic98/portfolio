<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="portfolio">
    <nav class="menu">
      <div class="logo-space"></div>
      <RouterLink class="nav-item" to="/"> Home </RouterLink>

      <RouterLink class="nav-item" to="/projects"> Projects </RouterLink>

      <RouterLink class="nav-item" to="/about"> About </RouterLink>
    </nav>
    <main class="main-window">
      <RouterView />
    </main>
  </div>
</template>

<style>
@import "@/assets/base.css";

.portfolio {
  display: grid;
  grid-template-columns: 1fr 4fr;
  height: 100vh;
  background-color: var(--main-background);
}
.main-window {
  padding: 4%;
  overflow-y: scroll;
}
/* Menu */
.menu {
  background-color: rgb(66, 66, 66);
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 15vh;
  align-content: start;
  font-family: monospace;
  /* justify-items: center; */
}
.nav-item {
  color: white;
  text-decoration: none;
  font-size: 1.5rem;
  padding: 10px;
  padding-left: 10%;
}
.router-link-active {
  background-color: var(--main-background);
  color: var(--primary);
}
</style>
