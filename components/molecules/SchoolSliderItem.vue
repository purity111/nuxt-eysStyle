<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  titleEn?: string;
  titleJp?: string;
  imgUrl?: string;
  logo?: string;
  schoolLink?: string;
}>();
</script>

<template>
  <div class="relative w-max">
    <div class="absolute top-[6px] left-0">
      <p class="text-xs lg:text-lg font-medium">{{ titleEn }}</p>
      <p class="text-[13px] lg:text-lg font-medium">{{ titleJp }}</p>
    </div>
    <img
      :src="imgUrl"
      class="h-[265px] lg:h-[420px] ml-[7px] lg:ml-[10px] mb-[15px] lg:mb-[30px]"
      alt="スクールスライダー"
      loading="lazy"
      decoding="async"
    />
    <div class="absolute bottom-[-14px] left-[52%] -translate-x-1/2">
      <AtomsEllipseLogo :imgUrl="logo" />
      <AtomsToClassTop
        :text="'スクールTOPへ'"
        class="w-[160px] h-[28px] lg:w-[240px] lg:h-[50px] mt-[-20px]"
      />
    </div>
  </div>
</template>
