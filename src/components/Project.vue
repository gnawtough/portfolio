<script setup>
const props = defineProps({
  project: Object
});

</script>

<template>
  <div class="project-tile">
    <img :src="props.project.imageUrl" class="project-image" alt="Bingus">
    <h3 class="project-text">{{ props.project.title }}</h3>
    <p class="project-text">{{ props.project.description }}</p>
  </div>
</template>

<style scoped>
.project-tile {
  background: #282828;
  margin-right: 20px; /* Space between tiles */
  width: 200px;
  border-radius: 20px;
}

.project-image {
  width: 90%;
  height: auto; /* Maintain aspect ratio */
  margin: 20px 20px 20px 10px;
  border-radius: 20px;
}

.project-text {
  margin: 0 0 0 10px;
}
</style>
