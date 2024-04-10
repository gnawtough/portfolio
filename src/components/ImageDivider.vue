<script setup>

</script>

<template>
  <div class="image-divider">
    <img src="@/assets/divider-image.svg" alt="Divider" />
  </div>
</template>

<script>
export default {
  name: 'ImageDivider',
  // props or data go here
}
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
