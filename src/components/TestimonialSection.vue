<script setup lang="ts">
import ReviewSection from "@/components/ReviewSection.vue";

const title = "Testimoniale"
const subtitle = "păreri despre produsele noastre"
</script>

<template>
  <div class="testimonial-section">
    <h2 class="testimonial-title">{{ title }}</h2>
    <h3 class="testimonial-subtitle">{{ subtitle }}</h3>
  </div>

  <ReviewSection />
</template>

<style scoped lang="postcss">
.testimonial-section {
  @apply flex flex-col items-center 2xl:my-12;
}
.testimonial-title {
  @apply text-[#333] font-semibold text-[30px];
}
.testimonial-subtitle {
  @apply text-[#563A15]/50 text-[25px] text-center uppercase;
}
</style>