<template>
  <div class="slit-container" ref="slitContainer">
    <img src="@/assets/ScrollingPlaceHolder.jpg" alt="Scrolling Image" class="panning-image">
  </div>
</template>

<script>
export default {
  props: {
    imageTop: Number,
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const containerRect = this.$refs.slitContainer.getBoundingClientRect();
      const containerTop = containerRect.top;
      const containerHeight = containerRect.height;

      // Determine the scroll position within the viewport
      const scrollPosition = window.scrollY;
      const viewportHeight = window.innerHeight;

      // Calculate the image's position based on the scroll position
      let imagePosition = 0;
      if (containerTop < viewportHeight && containerTop + containerHeight > 0) {
        // Image moves when the slit container is within the viewport
        imagePosition = (containerTop / viewportHeight) * 100;
      }

      // Apply the calculated position to the image
      this.$refs.slitContainer.children[0].style.transform = `translateY(${imagePosition}%)`;
    },
  },
};
</script>

<style scoped>
.slit-container {
  overflow: hidden;
  position: relative;
  height: 100px; /* Height of the slit through which the image is visible */
  width: 100%;
}

.panning-image {
  position: absolute;
  top: -50%; /* Start position of the image to ensure it moves through the slit */
  left: 0;
  width: 100%;
  transition: transform 0.3s ease-out; /* Smooth transition for the panning effect */
}
</style>