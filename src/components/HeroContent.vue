<script setup lang="ts">
import DiscoverButton from "@/components/DiscoverButton.vue";

const title = "Tortinella"
const subtitle = "Bakery"
const motto = "Gustul care transformă orice zi \n" +
    "    într-o sărbătoare"
</script>

<template>
  <div class="hero-content">
    <span class="title">{{ title }}</span>
    <span class="subtitle">{{ subtitle }}</span>
    <span class="motto">{{ motto }}</span>
    <DiscoverButton class="mt-12"></DiscoverButton>
  </div>
</template>

<style scoped lang="postcss">
.hero-content {
  @apply text-white flex flex-col justify-center h-full items-center;
}

.title {
  @apply text-[72px] font-medium;
}

.subtitle {
  @apply text-[#FFA429] text-[32px];
}

.motto {
  @apply text-[24px] 2xl:text-[40px] whitespace-pre-line text-center;
}
</style>