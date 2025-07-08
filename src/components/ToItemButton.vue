<script setup lang="ts">
import {ref} from 'vue';

const isHovered = ref(false);
</script>

<template>
  <button class="item-button"
          @mouseenter="isHovered = true"
          @mouseleave="isHovered = false"
  >
    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M5 12H19" :stroke="isHovered ? '#fff' : '#BC7E2D'" stroke-width="2" stroke-linecap="round"
            stroke-linejoin="round"/>
      <path d="M12 5L19 12L12 19" :stroke="isHovered ? '#fff' : '#BC7E2D'" stroke-width="2" stroke-linecap="round"
            stroke-linejoin="round"/>
    </svg>
  </button>
</template>

<style scoped lang="postcss">
.item-button {
  @apply 2xl:w-16 2xl:h-16 2xl:bg-white/90 2xl:rounded-full 2xl:flex 2xl:items-center 2xl:justify-center 2xl:z-50 2xl:hover:bg-[#BC7E2D];
}
</style>