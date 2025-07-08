<script setup lang="ts">
import background from "@/assets/images/motto-section.jpg"

const motto = "“Dulce simplu, gust desăvârșit“"
</script>

<template>
  <div
      class="relative w-screen -z-20 bg-cover bg-center bg-no-repeat"
      :style="{ backgroundImage: `url(${background})` }"
  >
    <div class="absolute -z-10 inset-0 bg-[#333]/50"></div>
    <div>
      <h2 class="text-white/80 text-[30px] z-10 text-center py-16">{{ motto }}</h2>
    </div>
  </div>
</template>