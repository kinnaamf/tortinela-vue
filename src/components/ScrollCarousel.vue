<script setup lang="ts">
import DarkIcon from "@/components/icons/DarkIcon.vue";
import BrightIcon from "@/components/icons/BrightIcon.vue";
</script>

<template>
  <div class="select-none">
    <div v-for="(item, index) in 10" :key="index" class="text-[20px] font-medium">
      <div v-if="index%2===0" class="carousel-content">
        <DarkIcon/>
        sărbători de iarna
      </div>
      <div v-if="index%2!==0" class="carousel-content">
        <BrightIcon/>
        Reduceri până la 40%
      </div>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.carousel-content {
  @apply 2xl:uppercase 2xl:flex 2xl:items-center 2xl:gap-1;
}
</style>