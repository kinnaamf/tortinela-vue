<script setup lang="ts">
import background from "@/assets/images/motto-section.jpg"

const motto = "“Dulce simplu, gust desăvârșit“"
</script>

<template>
  <div
      class="motto-section"
      :style="{ backgroundImage: `url(${background})` }"
  >
    <div class="dark-overlay"></div>
    <div>
      <h2 class="motto">{{ motto }}</h2>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.motto-section {
  @apply 2xl:relative 2xl:w-screen 2xl:-z-20 2xl:bg-cover 2xl:bg-center 2xl:bg-no-repeat;
}

.dark-overlay {
  @apply 2xl:absolute 2xl:-z-10 2xl:inset-0 2xl:bg-[#333]/50;
}

.motto {
  @apply 2xl:text-white/80 2xl:text-[30px] 2xl:z-10 2xl:text-center 2xl:py-16;
}
</style>