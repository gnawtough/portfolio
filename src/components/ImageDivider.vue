<script setup>
defineProps({
  image: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="image-divider">
    <img :src=image alt="Divider" />
  </div>
</template>

<script>
</script>

<style scoped>
.image-divider {
  width: 100%;
  display: flex;
  justify-content: center;
  margin: 20px 0;
}

.image-divider img {
  max-width: 100%;
  height: auto;
}
</style>
