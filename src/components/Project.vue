<template>
  <div class="project-tile">
    <img :src="project.imageUrl" alt="" class="project-image">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    project: Object
  }
};
</script>

<style scoped>
.project-tile {
  margin-right: 20px; /* Space between tiles */
  width: 200px; /* Or any specific width */
}

.project-image {
  width: 100%;
  height: auto; /* Maintain aspect ratio */
}
</style>
