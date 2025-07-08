<script setup lang="ts">
import DarkIcon from "@/components/icons/DarkIcon.vue";
import BrightIcon from "@/components/icons/BrightIcon.vue";
</script>

<template>
  <div class="">
    <div v-for="(item, index) in 10" :key="index" class="text-[20px] font-medium">
      <div v-if="index%2===0" class="uppercase flex items-center gap-1">
        <DarkIcon/>
        sărbători de iarna
      </div>
      <div v-if="index%2!==0" class="uppercase flex items-center gap-1">
        <BrightIcon/>
        Reduceri până la 40%
      </div>
    </div>
  </div>
</template>
