<template>
  <div class="product-grid">
    <div
        v-for="(product, index) in products"
        :key="index"
        class="product-card"
        :style="{
        backgroundImage: 'url(' + product.image + ')',
        gridArea: product.area,
      }"
        @mouseenter="hoveredIndex = index"
        @mouseleave="hoveredIndex = null"
    >
      <div
          class="product-overlay"
          :class="hoveredIndex === index ? '2xl:opacity-0 2xl:pointer-events-none' : '2xl:opacity-100 2xl:pointer-events-auto'"
      >
        <div class="product-darken"></div>
        <div
            class="product-discount-badge"
        >
          <div class="discount-text">
            <span>{{ product.discount }}%</span>
            <span class="text-[14px] font-normal">off</span>
          </div>
        </div>
        <div
            class="product-info"
        >
          <span>{{ product.title }}</span>
          <span>{{ product.weight }}</span>
        </div>
      </div>

      <ToItemButton
          class="product-button"
          :class="hoveredIndex === index ? 'opacity-100' : 'opacity-0 pointer-events-none'"
      />
    </div>
  </div>
</template>


<script setup lang="ts">
import image1 from "@/assets/images/bakery/image1.png"
import image2 from "@/assets/images/bakery/image2.png"
import image3 from "@/assets/images/bakery/image3.png"
import image4 from "@/assets/images/bakery/image4.png"
import image5 from "@/assets/images/bakery/image5.png"
import {ref} from "vue";
import ToItemButton from "@/components/ToItemButton.vue";

const hoveredIndex = ref<number | null>(null);

const products = [
  {
    title: "Set de prăjituri\nDE AUTOR",
    weight: '35g',
    discount: 35,
    image: image1,
    area: '1 / 1 / 2 / 3'
  },
  {
    title: "Tabletă mini din ciocolată belgiană\n(în sortiment) ",
    weight: '35g',
    discount: 10,
    image: image2,
    area: '1 / 3 / 2 / 5'
  },
  {
    title: "Cușma lui\nGUGUȚĂ",
    weight: '600g',
    discount: 40,
    image: image3,
    area: '1 / 5 / 3 / 7'
  },
  {
    title: "Tort KIEV\n(seria „Amintiri”)",
    weight: '600g',
    discount: 20,
    image: image4,
    area: '2 / 1 / 3 / 3'
  },
  {
    title: "Jeleu Chia\nCU CĂPȘUNĂ",
    weight: '170g',
    discount: 25,
    image: image5,
    area: '2 / 3 / 3 / 5'
  },
]
</script>

<style scoped lang="postcss">
.product-grid {
  @apply 2xl:grid 2xl:grid-cols-6 2xl:grid-rows-2 2xl:h-[540px] gap-4 text-white flex flex-col;
}

.product-card {
  @apply relative rounded-lg overflow-hidden bg-no-repeat bg-cover bg-center 2xl:cursor-pointer 2xl:h-full h-96;
}

.product-overlay {
  @apply 2xl:absolute 2xl:inset-0 2xl:transition-opacity 2xl:duration-300;
}

.product-darken {
  @apply absolute inset-0 bg-[#333]/50;
}

.product-discount-badge {
  @apply 2xl:absolute 2xl:top-3 2xl:right-3 2xl:bg-white 2xl:text-black 2xl:w-24 2xl:font-bold 2xl:h-24 2xl:rounded-full 2xl:flex 2xl:justify-center 2xl:items-center hidden ;
}

.discount-text {
  @apply 2xl:text-center 2xl:leading-tight 2xl:text-[30px] 2xl:flex 2xl:flex-col 2xl:select-none;
}

.product-info {
  @apply z-10 text-white absolute bottom-3 left-3 whitespace-pre-line text-[18px] flex flex-col font-semibold;
}

.product-button {
  @apply absolute inset-0 top-[50%] left-[50%] translate-y-[-50%] translate-x-[-50%] transition-opacity duration-300;
}

</style>
