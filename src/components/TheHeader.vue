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
  @apply 2xl:flex 2xl:justify-between 2xl:items-center 2xl:px-36 2xl:py-3
}
</style>