<script setup>
import Intro from './components/Introduction.vue'
import LandingPage from "@/components/LandingPage.vue";
import ImageDivider from "@/components/ImageDivider.vue";
</script>

<template>
  <header>
    <img alt="Rat logo" class="logo" src="./assets/logoRat.svg" width="125" height="125" />

    <div class="wrapper">
      <Intro msg="Andrew Koller" />
    </div>
  </header>

  <ImageDivider image="@/assets/logo.svg" />

  <main>
    <LandingPage />
  </main>
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
    display: inline-flex;
    place-items: flex-start;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: inline-flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
