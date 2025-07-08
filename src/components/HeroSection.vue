<script setup lang="ts">
import background from "@/assets/images/background.jpg"
import HeroContent from "@/components/HeroContent.vue";
</script>

<template>
  <div class="hero-wrapper"
       :style="{ backgroundImage: `url(${background})` }">
    <div class="hero-overlay"></div>
    <div class="hero-content">
      <HeroContent></HeroContent>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.hero-wrapper {
  @apply 2xl:relative 2xl:w-full 2xl:h-[80vh] 2xl:bg-cover 2xl:bg-center;
}

.hero-overlay {
  @apply 2xl:absolute 2xl:inset-0 2xl:bg-black/60 2xl:z-10;
}

.hero-content {
  @apply 2xl:relative 2xl:z-10 2xl:h-full;
}
</style>