<template>
  <div class="flex flex-col">
    <TheHeader/>
    <div class="flex flex-col gap-12">
      <HeroSection/>
      <PromotionsSection/>
      <MottoSection/>
      <TestimonialSection/>
    </div>
  </div>
  <div class="w-screen bg-white h-[100px]"></div>
</template>

<script setup lang="ts">

import TheHeader from "@/components/TheHeader.vue";
import HeroSection from "@/components/HeroSection.vue";
import PromotionsSection from "@/components/PromotionsSection.vue";
import MottoSection from "@/components/MottoSection.vue";
import TestimonialSection from "@/components/TestimonialSection.vue";
</script>

<style scoped>

</style>