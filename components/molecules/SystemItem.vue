<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  num?: string;
  titleCaption?: string;
  title?: string;
  imgUrl?: string;
  tblTitle?: string;
  tblData?: {
    course: number[];
    cost: number[];
  };
}>();

</script>

<template>
  <div
    class="relative w-[174px] lg:w-[320px] m-auto bg-white border border-[#DDDDDD]"
  >
    <div class="pt-[12px] lg:pt-[37px]">
      <h5
        v-html="props.titleCaption"
        class="text-center text-[10px] lg:text-[13px] pb-[5px] lg:pb-[10px]"
      ></h5>
      <h3 v-html="props.title" class="text-center text-[16px] lg:text-[28px]"></h3>
      <img
        class="w-full pt-[5px] lg:pt-[30px]"
        :src="props.imgUrl"
        alt="イメージ"
        loading="lazy"
        decoding="async"
      />
    </div>
    <h1
      class="absolute top-[-20px] lg:top-[-50px] left-[50%] leading-none -translate-x-1/2 text-center text-[40px] lg:text-[80px] text-[#FAB6B0]"
    >
      {{ props.num }}
    </h1>
    <div class="hidden lg:block px-[10px]">
      <img
        class="m-auto py-[20px]"
        src="/img/pc/system-icon.svg"
        alt="arrow"
        loading="lazy"
        decoding="async"
      />
      <h5 class="text-[18px] text-center font-medium" v-html="props.tblTitle"></h5>
      <AtomsTable
        :course="props.tblData?.course"
        :cost="props.tblData?.cost"
        class="mt-[20px]"
      />
    </div>
  </div>
</template>
