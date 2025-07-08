<script setup lang="ts">
import type { PropType } from "vue";

interface Review {
  content: string;
  userImage: string;
  userName: string;
}

const props = defineProps<{
  review: Review;
}>();
</script>

<template>
  <div class="review-content">
    <h2 v-html="review.content" class="review-text"></h2>
    <img :src="review.userImage" alt="User photo" class="review-avatar" />
    <h2 class="review-username">{{ review.userName }}</h2>

    <slot />
  </div>
</template>

<style scoped lang="postcss">
.review-content {
  @apply flex flex-col items-center max-w-3xl mx-auto text-center relative;
}

.review-text {
  @apply text-[20px] leading-relaxed;
}

.review-avatar {
  @apply h-24 w-24 object-cover rounded-full mt-2 mb-2 opacity-70;
}

.review-username {
  @apply text-lg font-semibold uppercase;
}
</style>
