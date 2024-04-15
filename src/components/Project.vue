<script setup>
const props = defineProps({
  project: Object
});

</script>

<template>
  <div class="project-tile">
    <div class="image-container">
      <img :src="props.project.imageUrl" class="project-image" alt="Bingus">
    </div>
    <h3 class="project-text">{{ props.project.title }}</h3>
    <p class="project-text">{{ props.project.description }}</p>
  </div>
</template>

<style scoped>
.project-tile {
  background: #282828;
  margin-right: 1rem; /* Space between tiles */
  width: 12rem;
  border-radius: 1rem;
  overflow: hidden;
}

.project-tile:hover {
  background: green;
}

.image-container {
  width: 100%; /* Full width of the tile */
  height: 10rem; /* Fixed height for the image */
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; /* Clip the image if it's too large */
  margin-top: 1rem;
}

.project-image {
  width: auto;
  height: 100%;
  max-width: 100%;
  border-radius: 1rem;
}

.project-text {
  margin: 0 1rem 1rem 1rem;
}
</style>
