<script setup lang="ts">
import ProductGrid from "@/components/ProductGrid.vue";
import ScrollCarousel from "@/components/ScrollCarousel.vue";

const title = "Promoțiile de Weekend"
const discount = "până la 40% reducere "
</script>

<template>
  <div>
    <div class="flex flex-col items-center">
      <h2 class="text-[#333] font-semibold text-[30px]">{{ title }}</h2>
      <h3 class="text-[#563A15]/50 text-[25px] uppercase">{{ discount }}</h3>
    </div>
    <ProductGrid class="px-20 mt-8"></ProductGrid>
    <ScrollCarousel class="mt-16 flex items-center text-nowrap gap-8 overflow-x-hidden"/>
  </div>
</template>