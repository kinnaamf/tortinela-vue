<script setup lang="ts">
import ReviewSection from "@/components/ReviewSection.vue";

const title = "Testimoniale"
const subtitle = "păreri despre produsele noastre"
</script>

<template>
  <div class="flex flex-col items-center my-12">
    <h2 class="text-[#333] font-semibold text-[30px]">{{ title }}</h2>
    <h3 class="text-[#563A15]/50 text-[25px] uppercase">{{ subtitle }}</h3>
  </div>

  <ReviewSection/>
</template>