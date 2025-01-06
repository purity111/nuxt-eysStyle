<script setup lang="ts">
import { defineProps } from 'vue';
const props = defineProps<{
    feature?: string,
    title?: string
}>();

</script>

<template>
  <div class="group w-[50%] grid lg:h-[80px] h-[50px] relative border border-[#DDDDDD] border-t-0 hover:border-b-0 hover:bg-white">
   <div class="flex justify-center items-center flex-col gap-[5px]">
    <p class="lg:text-[11px] text-[8px] tracking-[0.25em]">{{ props.feature }}</p>
    <h5 class="lg:text-[18px] text-[12px]">{{ props.title }}</h5>
   </div>
    <img
      class="smooth lg:w-[25px] w-[14px] absolute lg:top-[27px] lg:right-[37px] top-[16px] right-[15px] group-hover:rotate-90" 
      src="/img/common/arrow-right.svg"
      alt="メニューアイテム"
      loading="lazy"
      decoding="async"
    />
  </div>
</template>

<style scoped>
.smooth {
    transition: .4s ease;
}
</style>