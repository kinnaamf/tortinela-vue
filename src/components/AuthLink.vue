<script setup lang="ts">
import UserIcon from "@/components/icons/UserIcon.vue";
</script>

<template>
  <button class="account-button">
    <UserIcon/>
    <h3>Contul meu</h3>
  </button>
</template>

<style scoped lang="postcss">
.account-button {
  @apply 2xl:flex 2xl:gap-3 2xl:opacity-30 2xl:items-center 2xl:font-normal;
}
</style>