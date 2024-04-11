<script setup>

</script>

<template>
  <div>
    <Category v-for="category in categories" :key="category.id" :category="category" />
  </div>
</template>

<script>
import { categories } from '@/data/projectData.js';
import Category from './Category.vue';

export default {
  components: {
    Category
  },
  data() {
    return {
      categories
    };
  }
};
</script>

