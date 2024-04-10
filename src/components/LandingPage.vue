<script setup>
import Category from "@/components/Category.vue";
import LogoRat from "@/components/icons/IconCommunity.vue";
</script>

<template>
  <Category>
    <template #preview>
      <LogoRat />
    </template>

    <template #title>My Projects</template>

    This is a section I added that is for the one and only
    <a href="https://en.wikipedia.org/wiki/Crash_Bandicoot" target="_blank" rel="noopener">Crash</a>
    .
  </Category>

  <Category>
    <template #title>Second Item</template>
  </Category>

</template>
