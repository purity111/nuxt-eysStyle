<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  price?: number;
}>();
</script>

<template>
  <div class="hiragino-sans text-white">
    <div class="flex justify-start">
      <h2
        class="roboto italic font-black leading-none roboto pl-[3px] pr-[5px] text-[37px] lg:text-[60px]"
      >
        {{ props.price?.toLocaleString() }}
      </h2>
      <h3 class="leading-[2] text-[22px] lg:text-[40px]">エース</h3>
    </div>
    <div
      class="bg-white w-full h-[2px] lg:h-[4px] mt-[-4px] lg:mt-[-10px] mb-[4px] lg:mb-[10px]"
    ></div>
    <h3 class="leading-none pl-[10px] text-[22px] lg:text-[40px]">
      プレゼント!!
    </h3>
  </div>
</template>
