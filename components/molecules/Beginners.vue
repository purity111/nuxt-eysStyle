<template>
  <div class="relative w-full mt-[93px] max-lg:mt-[47px]">
    <h3
      class="text-[30px] text-center max-lg:text-lg font-medium !leading-none"
    >
      {{ workshop.title }}
    </h3>
    <div
      class="w-full max-w-[1000px] lg:mx-auto mt-[38px] max-lg:mt-[20px] pl-[30px] lg:pl-0"
    >
      <Swiper
        v-if="workshop"
        :modules="[Navigation]"
        :navigation="{
          nextEl: '.beginner-swiper-button-next',
          prevEl: '.beginner-swiper-button-prev',
        }"
        :loop="true"
        :breakpoints="{
          320: {
            slidesPerView: 1.4,
            spaceBetween: 15,
          },
          1024: {
            slidesPerView: 5.1,
            spaceBetween: 30,
          },
        }"
        class="lg:min-w-[1750px]"
      >
        <SwiperSlide v-for="(item, i) of workshop?.items" :key="i">
          <AtomsWorkShop :workshop="item" />
        </SwiperSlide>
      </Swiper>
    </div>
    <button
      class="beginner-swiper-button-prev absolute bg-[#00000080] top-[50%] left-0 w-[80px] max-lg:w-[40px] aspect-square z-10 content-center"
    >
      <img
        src="/img/pc/slide-arrow-left.svg"
        alt="left"
        class="-rotate-90 mx-auto max-lg:w-[8px]"
      />
    </button>
    <button
      class="beginner-swiper-button-next absolute bg-[#00000080] top-[50%] right-0 w-[80px] max-lg:w-[40px] aspect-square z-10 content-center"
    >
      <img
        src="/img/pc/slide-arrow-right.svg"
        alt="right"
        class="-rotate-90 mx-auto max-lg:w-[8px]"
      />
    </button>
  </div>
</template>
<script setup lang="ts">
import { Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import type { Workshop } from "./Workshop.vue";

defineProps<{
  workshop: Workshop;
}>();
</script>
