<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>

    <template #heading>My Projects</template>

    This is a section I added that is for the one and only
    <a href="https://en.wikipedia.org/wiki/Crash_Bandicoot" target="_blank" rel="noopener">Crash</a>
    .
  </WelcomeItem>
</template>
