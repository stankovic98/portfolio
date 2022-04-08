<template>
  <div class="project">
    <img src="https://picsum.photos/200/300" alt="Preview of project" />
    <div class="overlay">
      <h3>Project name</h3>
      <p>
        Description in a few words, <a href="#">blog post</a>, if you want to
        know more
      </p>
      <button>View</button>
    </div>
  </div>
</template>

<style scoped>
.project {
  border: 3px solid var(--primary);
  border-radius: 5px;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr;
  overflow: hidden;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  grid-row: 1 / -1;
  grid-column: 1 / -1;
}
.overlay {
  position: relative;
  background-color: rgba(224, 235, 72, 0.747);
  grid-row: 1 / -1;
  grid-column: 1 / -1;
  display: grid;
  align-content: center;
  justify-items: center;
  grid-gap: 10px;
  padding: 20px;
  color: grey;
  font-size: 1.2rem;
  transition: 0.3s;
  transform: translateY(100%);
}

.project:hover .overlay {
  transform: translateY(0);
}
</style>
