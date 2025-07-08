<script setup lang="ts">
import ProductGrid from "@/components/ProductGrid.vue";
import ScrollCarousel from "@/components/ScrollCarousel.vue";

const title = "Promoțiile de Weekend"
const discount = "până la 40% reducere "
</script>

<template>
  <div class="promo-section">
    <div class="promo-heading">
      <h2 class="promo-title">{{ title }}</h2>
      <h3 class="promo-discount">{{ discount }}</h3>
    </div>
    <ProductGrid class="promo-products"/>
    <ScrollCarousel class="promo-carousel"/>
  </div>
</template>

<style scoped lang="postcss">
.promo-heading {
  @apply flex flex-col items-center;
}

.promo-title {
  @apply text-[#333] font-semibold text-[30px];
}

.promo-discount {
  @apply text-[#563A15]/50 text-[25px] uppercase;
}

.promo-products {
  @apply 2xl:px-20 mt-8;
}

.promo-carousel {
  @apply mt-8 2xl:mt-16 flex items-center text-nowrap gap-8 overflow-x-hidden;
}

</style>
