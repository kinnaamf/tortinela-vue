<script setup lang="ts">
import {ref} from 'vue';

const isHovered = ref(false);
</script>

<template>
  <button class="w-16 h-16 bg-white/90 rounded-full flex items-center justify-center z-50 hover:bg-[#BC7E2D]"
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
