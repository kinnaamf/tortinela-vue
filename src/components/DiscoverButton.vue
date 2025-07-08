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
  @apply bg-[#BC7E2D] px-8 2xl:px-12 py-5 uppercase rounded-full 2xl:hover:bg-[#333] 2xl:transition-all;
}
</style>