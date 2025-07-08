<template>
  <div class="grid grid-cols-6 h-[540px] gap-4 text-white">
    <div
        v-for="(product, index) in products"
        :key="index"
        class="relative rounded-lg overflow-hidden bg-no-repeat bg-cover bg-center group"
        :style="{
        backgroundImage: 'url(' + product.image + ')',
        gridArea: product.area,
      }"
        @mouseenter="hoveredIndex = index"
        @mouseleave="hoveredIndex = null"
    >
      <div
          class="absolute inset-0 transition-opacity duration-300"
          :class="hoveredIndex === index ? 'opacity-0 pointer-events-none' : 'opacity-100 pointer-events-auto'"
      >
        <div class="absolute inset-0 bg-[#333]/50"></div>
        <div
            class="absolute top-3 right-3 bg-white text-black w-24 font-bold h-24 rounded-full flex justify-center items-center"
        >
          <div class="text-center leading-tight text-[30px] flex flex-col">
            <span>{{ product.discount }}%</span>
            <span class="text-[14px] font-normal">off</span>
          </div>
        </div>
        <div
            class="z-10 text-white absolute bottom-3 left-3 whitespace-pre-line text-[18px] flex flex-col font-semibold"
        >
          <span>{{ product.title }}</span>
          <span>{{ product.weight }}</span>
        </div>
      </div>

      <ToItemButton
          class="absolute inset-0 top-[50%] left-[50%] translate-y-[-50%] translate-x-[-50%] transition-opacity duration-300"
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
