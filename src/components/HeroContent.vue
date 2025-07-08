<script setup lang="ts">
import DiscoverButton from "@/components/DiscoverButton.vue";

const title = "Tortinella"
const subtitle = "Bakery"
const motto = "Gustul care transformă orice zi \n" +
    "    într-o sărbătoare"
</script>

<template>
  <div class="text-white flex flex-col justify-center h-full items-center ">
    <span class="text-[72px] font-medium">{{ title }}</span>
    <span class="text-[#FFA429] text-[32px]">{{ subtitle }}</span>
    <span class="text-[40px] whitespace-pre-line text-center">{{ motto }}</span>
    <DiscoverButton class="mt-12"></DiscoverButton>
  </div>
</template>