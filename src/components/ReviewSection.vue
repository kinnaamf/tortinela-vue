<script setup lang="ts">
import {ref} from "vue";
import background from "@/assets/images/review-section.jpg";
import ArrowIcon from "@/components/icons/ArrowIcon.vue";
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
    userName: "Muntean viorel",
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
    userName: "cacinshi cristina",
  },
];

function prev() {
  activeIndex.value =
      (activeIndex.value - 1 + reviews.length) % reviews.length;
}

function next() {
  activeIndex.value = (activeIndex.value + 1) % reviews.length;
}
</script>

<template>
  <div
      class="relative px-60 py-20 h-[470px] bg-center bg-cover"
      :style="{ backgroundImage: `url(${background})` }"
  >
    <div
        class="relative bg-white/80 h-[330px] z-20 pt-12 pb-6 px-12 items-center flex justify-between gap-8">
      <!-- Prev -->
      <button @click="prev" class="hover:scale-110 transition relative z-20">
        <ArrowIcon/>
      </button>

      <!-- Review -->
      <div class="flex flex-col items-center gap-4">
        <div
            v-if="reviews.length"
            class="flex flex-col items-center max-w-3xl mx-auto text-center"
        >
          <h2
              v-html="reviews[activeIndex].content"
              class="text-[20px] leading-relaxed"
          ></h2>
          <img
              :src="reviews[activeIndex].userImage"
              class="h-24 w-24 object-cover rounded-full mt-2 mb-2 opacity-70"
              alt=""
          />
          <h2 class="text-lg font-semibold uppercase">
            {{ reviews[activeIndex].userName }}
          </h2>

          <!-- Dots -->

        </div>

        <div class="flex gap-[6px] absolute bottom-4">
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
      <!-- Next -->
      <button @click="next" class="rotate-180 hover:scale-110 transition relative z-20">
        <ArrowIcon/>
      </button>
    </div>
    <div class="absolute inset-0 bg-[#333]/50 "></div>
  </div>
</template>