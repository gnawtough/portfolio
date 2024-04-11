<script setup>
import { ref } from 'vue';
import Category from './Category.vue';
import { categories as categoriesData } from '@/data/projectData.js';

const categories = ref(categoriesData);
</script>

<template>
  <div>
    <Category v-for="category in categories" :key="category.id" :category="category" />
  </div>
</template>
