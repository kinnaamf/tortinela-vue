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
  @apply relative w-full z-0 2xl:h-[80vh] bg-cover bg-center h-[60vh];
}

.hero-overlay {
  @apply absolute inset-0 bg-black/60 -z-10;
}

.hero-content {
  @apply relative z-10 h-full;
}
</style>