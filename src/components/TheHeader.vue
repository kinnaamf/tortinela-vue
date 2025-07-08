<script setup lang="ts">

import TheLogo from "@/components/TheLogo.vue";
import HeaderNav from "@/components/HeaderNav.vue";
import AuthLink from "@/components/AuthLink.vue";
import MenuIcon from "@/components/icons/MenuIcon.vue";
import CloseMenuIcon from "@/components/icons/CloseMenuIcon.vue";
import {ref} from "vue";

const isClicked = ref(false)
</script>

<template>
  <header class="header">
    <TheLogo class="logo"/>
    <HeaderNav class="header-nav"></HeaderNav>
    <AuthLink class="auth-link"></AuthLink>
    <MenuIcon class="menu-icon" @click="isClicked = true"/>
  </header>

  <div class="2xl:hidden the-menu" :class="isClicked ? 'translate-x-0  transition-all duration-300' : 'translate-x-[400px] transition-all duration-300'">
    <CloseMenuIcon class="2xl:hidden absolute right-8 top-3" @click="isClicked = false"/>
    <div class="absolute right-8 top-10 text-left flex flex-col items-end gap-2 text-2xl">
      <HeaderNav/>
      <AuthLink class="flex items-center gap-4"/>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.header {
  @apply flex justify-between items-center 2xl:px-36 2xl:py-3
          px-8
}
.header-nav {
  @apply 2xl:flex
        hidden
}
.menu-icon {
  @apply 2xl:hidden absolute right-8
}
.logo {
  @apply z-20 2xl:relative
}
.auth-link {
  @apply hidden 2xl:flex
}
.the-menu {
  @apply 2xl:hidden absolute bg-white z-50 h-screen w-screen z-10 flex justify-between px-8
}
</style>