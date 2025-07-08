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
  @apply 2xl:flex 2xl:flex-col 2xl:items-center 2xl:max-w-3xl 2xl:mx-auto 2xl:text-center 2xl:relative;
}

.review-text {
  @apply 2xl:text-[20px] 2xl:leading-relaxed;
}

.review-avatar {
  @apply h-16 w-16 2xl:h-24 2xl:w-24 object-cover rounded-full mt-2 mb-2 opacity-70;
}

.review-username {
  @apply text-lg mb-4 2xl:mb-0 font-semibold uppercase;
}
</style>
