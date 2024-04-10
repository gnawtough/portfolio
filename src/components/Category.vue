<script setup>
import Project from './Project.vue';
import { defineProps } from 'vue';

// Automatically infers the type based on the default value or initial call
const props = defineProps({
  category: Object
});
</script>

<template>
  <div class="category">
    <h2>{{ props.category.name }}</h2>
    <div class="projects-container">
      <Project v-for="project in props.category.projects" :key="project.id" :project="project" />
    </div>
  </div>
</template>

<style scoped>
.projects-container {
  display: flex;
  overflow-x: auto; /* Allows horizontal scrolling for overflow */
}
</style>
