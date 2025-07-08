<script setup lang="ts">
import background from "@/assets/images/background.jpg"
import HeroContent from "@/components/HeroContent.vue";
</script>

<template>
  <div class="relative w-full h-[80vh] bg-cover bg-center"
       :style="{ backgroundImage: `url(${background})` }">
    <div class="absolute inset-0 bg-black/60 z-10"></div>
    <div class="relative z-10 h-full">
      <HeroContent></HeroContent>
    </div>
  </div>
</template>