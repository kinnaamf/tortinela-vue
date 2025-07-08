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
  @apply 2xl:flex 2xl:flex-col 2xl:items-center;
}

.promo-title {
  @apply 2xl:text-[#333] 2xl:font-semibold 2xl:text-[30px];
}

.promo-discount {
  @apply 2xl:text-[#563A15]/50 2xl:text-[25px] 2xl:uppercase;
}

.promo-products {
  @apply 2xl:px-20 2xl:mt-8;
}

.promo-carousel {
  @apply 2xl:mt-16 2xl:flex 2xl:items-center 2xl:text-nowrap 2xl:gap-8 2xl:overflow-x-hidden;
}

</style>
