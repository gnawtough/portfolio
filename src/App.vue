<script setup>
import Intro from '@/components/Introduction.vue'
import Projects from "@/components/Projects.vue";
import ImageDivider from "@/components/ImageDivider.vue";
</script>

<template>
  <header>
    <img alt="Rat logo" class="logo" src="@/assets/logoRat.svg" width="125" height="125" />

    <div class="wrapper">
      <Intro msg="Andrew Koller" />
    </div>
  </header>

  <div>
    <ImageDivider />
  </div>

  <main>
    <div class="project">
      <Projects />
    </div>
  </main>

  <div>
    <ImageDivider />
  </div>
</template>

<style scoped>

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  .divider {
    display: inline-grid;
    margin: 0;
  }

  .category {
    display: inline-flex;
  }

  header .wrapper {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
