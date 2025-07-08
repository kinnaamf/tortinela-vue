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

      <ReviewContent :review="reviews[activeIndex]"/>

      <button @click="next" class="review-nav-button rotate-180" aria-label="Next review">
        <ArrowIcon/>
      </button>
    </div>

    <div class="review-overlay"></div>
  </div>
</template>

<style scoped lang="postcss">
.review-section {
  @apply relative px-60 py-20 h-[470px] bg-center bg-cover;
}

.review-container {
  @apply relative bg-white/80 h-[330px] z-20 pt-12 pb-6 px-12 flex items-center justify-between gap-8;
}

.review-nav-button {
  @apply hover:scale-110 transition relative z-20;
}

.review-overlay {
  @apply absolute inset-0 bg-[#333]/50;
}
</style>
