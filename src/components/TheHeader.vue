<script setup lang="ts">

import TheLogo from "@/components/TheLogo.vue";
import HeaderNav from "@/components/HeaderNav.vue";
import AuthLink from "@/components/AuthLink.vue";
</script>

<template>
  <header class="flex justify-between items-center px-36 py-3">
    <TheLogo/>
    <HeaderNav></HeaderNav>
    <AuthLink></AuthLink>
  </header>
</template>