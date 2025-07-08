<script setup lang="ts">

import TheLogo from "@/components/TheLogo.vue";
import HeaderNav from "@/components/HeaderNav.vue";
import AuthLink from "@/components/AuthLink.vue";
</script>

<template>
  <header class="header">
    <TheLogo/>
    <HeaderNav></HeaderNav>
    <AuthLink></AuthLink>
  </header>
</template>

<style scoped lang="postcss">
.header {
  @apply flex justify-between items-center px-36 py-3
}
</style>