<template>
  <div class="category">
    <h2>{{ category.name }}</h2>
    <div class="projects-container">
      <Project v-for="project in category.projects" :key="project.id" :project="project" />
    </div>
  </div>
</template>

<script>
import Project from './Project.vue';

export default {
  components: {
    Project
  },
  props: {
    category: Object
  }
};
</script>

<style scoped>
.projects-container {
  display: flex;
  overflow-x: auto; /* Allows horizontal scrolling for overflow */
}
</style>
