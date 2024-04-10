<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  project: Object
});

</script>

<template>
  <div class="project-tile">
    <img :src="props.project.imageUrl" class="project-image" alt="Bingus">
    <h3>{{ props.project.title }}</h3>
    <p>{{ props.project.description }}</p>
  </div>
</template>

<style scoped>
.project-tile {
  margin-right: 20px; /* Space between tiles */
  width: 200px;
}

.project-image {
  width: 100%;
  height: auto; /* Maintain aspect ratio */
}
</style>
