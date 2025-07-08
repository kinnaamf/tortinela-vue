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
  @apply text-white 2xl:flex 2xl:flex-col 2xl:justify-center 2xl:h-full 2xl:items-center;
}

.title {
  @apply 2xl:text-[72px] 2xl:font-medium;
}

.subtitle {
  @apply 2xl:text-[#FFA429] 2xl:text-[32px];
}

.motto {
  @apply 2xl:text-[40px] 2xl:whitespace-pre-line 2xl:text-center;
}
</style>