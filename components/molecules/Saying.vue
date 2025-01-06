<template>
  <div class="w-full relative">
    <div class="w-full max-lg:px-[20px]">
      <Swiper
        :modules="[Navigation]"
        :navigation="{
          nextEl: '.saying-swiper-button-next',
          prevEl: '.saying-swiper-button-prev',
        }"
        :loop="true"
        :breakpoints="{
          320: {
            slidesPerView: 1.3,
            spaceBetween: 15,
          },
          1024: {
            slidesPerView: 5.5,
            spaceBetween: 30,
            centeredSlides: true,
          },
        }"
        class="!overflow-visible"
      >
        <SwiperSlide v-for="(item, i) of sayings" :key="i">
          <AtomsSaying :item="item" />
        </SwiperSlide>
      </Swiper>
    </div>
    <button
      class="saying-swiper-button-prev absolute bg-[#00000080] top-[50%] left-0 lg:left-[340px] w-[80px] max-lg:w-[40px] aspect-square z-10 content-center"
    >
      <img
        src="/img/pc/slide-arrow-left.svg"
        alt="left"
        class="-rotate-90 mx-auto max-lg:w-[8px]"
      />
    </button>
    <button
      class="saying-swiper-button-next absolute bg-[#00000080] top-[50%] right-0 lg:right-[340px] w-[80px] max-lg:w-[40px] aspect-square z-10 content-center"
    >
      <img
        src="/img/pc/slide-arrow-right.svg"
        alt="right"
        class="-rotate-90 mx-auto max-lg:w-[8px]"
      />
    </button>
  </div>
</template>

<script lang="ts" setup>
import { Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import type { Saying } from "../atoms/Saying.vue";

defineProps<{
  sayings: Saying[];
}>();
</script>
