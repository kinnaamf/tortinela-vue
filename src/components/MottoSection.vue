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
  @apply relative w-screen -z-20 bg-cover bg-center bg-no-repeat;
}

.dark-overlay {
  @apply absolute -z-10 inset-0 bg-[#333]/50;
}

.motto {
  @apply text-white/80 text-[30px] z-10 text-center py-16;
}
</style>