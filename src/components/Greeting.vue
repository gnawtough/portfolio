<script setup>
defineProps({
  greetingMessage: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div>
    <h1> {{ greetingMessage }}</h1>
  </div>
</template>

<script>

</script>

<style scoped>
h1 {
  color: blue;
}
</style>