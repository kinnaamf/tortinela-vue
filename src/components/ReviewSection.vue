<script setup lang="ts">
import {ref} from "vue";
import background from "@/assets/images/review-section.jpg";
import ArrowIcon from "@/components/icons/ArrowIcon.vue";
import ReviewContent from "@/components/ReviewContent.vue";

import userImage1 from "@/assets/images/users/user1.png";
import userImage2 from "@/assets/images/users/user2.png";
import userImage3 from "@/assets/images/users/user3.png";
import userImage4 from "@/assets/images/users/user4.png";
import userImage5 from "@/assets/images/users/user5.png";

const activeIndex = ref(0);

const reviews = [
  {
    content:
        'Prăjiturile de la <span class="text-[#BC7E2D]">Tortinella</span> sunt absolut delicioase și mereu proaspete! Tortul personalizat a fost exact ce ne-am dorit, iar echipa a fost foarte amabilă și<br>atentă la detalii. Recomand cu încredere!',
    userImage: userImage1,
    userName: "Sabaciuc Ioana",
  },
  {
    content:
        'O adevărată încântare! <span class="text-[#BC7E2D]">Tortinella</span> are cele mai delicioase prăjituri pe care le-am gustat vreodată. Revin mereu cu drag!',
    userImage: userImage2,
    userName: "Muntean Viorel",
  },
  {
    content:
        '<span class="text-[#BC7E2D]">Tortinella</span> a fost alegerea noastră pentru tortul aniversar al fiicei mele, și a fost un succes total! Nu doar că a fost superb decorat, dar și gustul a fost extraordinar. Invitații au fost încântați, iar noi am rămas clienți fideli.',
    userImage: userImage3,
    userName: "Ardeleanu Irina",
  },
  {
    content:
        'Pentru mine, <span class="text-[#BC7E2D]">Tortinella</span> înseamnă mai mult decât deserturi – este o experiență. De fiecare dată când am poftă de ceva dulce sau vreau să fac o surpriză cuiva drag, apelez la ei.',
    userImage: userImage4,
    userName: "Belinski Marin",
  },
  {
    content:
        'Când vine vorba de dulciuri, sunt destul de pretențioasă, dar <span class="text-[#BC7E2D]">Tortinella</span> m-a cucerit complet! Deserturile lor sunt o combinație perfectă de savoare, textură și aspect.',
    userImage: userImage5,
    userName: "Cacinshi Cristina",
  },
];

function prev() {
  activeIndex.value = (activeIndex.value - 1 + reviews.length) % reviews.length;
}

function next() {
  activeIndex.value = (activeIndex.value + 1) % reviews.length;
}
</script>

<template>
  <div
      class="review-section"
      :style="{ backgroundImage: `url(${background})` }"
  >
    <div class="review-container">
      <button @click="prev" class="review-nav-button" aria-label="Previous review">
        <ArrowIcon/>
      </button>

      <div class="review-content">
        <ReviewContent :review="reviews[activeIndex]"/>
        <div class="dots-container">
          <button
              v-for="(review, i) in reviews"
              :key="i"
              @click="activeIndex = i"
              class="w-3 h-3 rounded-full transition-all duration-300"
              :class="activeIndex === i ? 'border-[#BC7E2D] border-2 bg-[#BC7E2D]/80 ' : 'bg-[#fff]'"
          >
          </button>
        </div>
      </div>

      <button @click="next" class="review-nav-button rotate-180" aria-label="Next review">
        <ArrowIcon/>
      </button>

    </div>

    <div class="review-overlay"></div>
  </div>
</template>

<style scoped lang="postcss">
.review-section {
  @apply 2xl:relative 2xl:px-60 2xl:py-20 2xl:h-[470px] 2xl:bg-center 2xl:bg-cover;
}

.review-container {
  @apply 2xl:relative 2xl:bg-white/80 2xl:h-[330px] 2xl:z-20 2xl:pt-12 2xl:pb-6 2xl:px-12 2xl:flex 2xl:items-center 2xl:justify-between 2xl:gap-8;
}

.review-nav-button {
  @apply 2xl:hover:scale-110 2xl:transition 2xl:relative 2xl:z-20;
}

.review-overlay {
  @apply 2xl:absolute 2xl:inset-0 2xl:bg-[#333]/50;
}
.review-content {
  @apply 2xl:flex 2xl:flex-col 2xl:items-center 2xl:gap-2;
}
.dots-container {
  @apply 2xl:flex 2xl:gap-2 2xl:absolute 2xl:bottom-4;
}
</style>
