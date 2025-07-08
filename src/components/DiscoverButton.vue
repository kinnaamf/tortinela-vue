<script setup lang="ts">
const buttonText = "Descoperă"
</script>

<template>
  <button class="discover-button">
    {{ buttonText }}
  </button>
</template>

<style scoped lang="postcss">
.discover-button {
  @apply 2xl:bg-[#BC7E2D] 2xl:px-12 2xl:py-5 2xl:uppercase 2xl:rounded-full 2xl:hover:bg-[#333] 2xl:transition-all;
}
</style>