<script setup>
</script>
<template>
  <div class="item">
    <i>
      <slot name="preview"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="title"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>

</style>
