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
  @apply 2xl:flex 2xl:flex-col 2xl:items-center 2xl:my-12;
}
.testimonial-title {
  @apply 2xl:text-[#333] 2xl:font-semibold 2xl:text-[30px];
}
.testimonial-subtitle {
  @apply 2xl:text-[#563A15]/50 2xl:text-[25px] 2xl:uppercase;
}
</style>