<template>
  <div class="h-auto w-[235px] lg:w-[320px] border border-[#DDDDDD]">
    <div class="w-full relative">
      <img :src="workshop.banner" class="w-full h-auto" />
      <p
        class="clip-board w-max text-[11px] font-semibold p-[8px_30px_8px_10px] bg-[#98CAF5] text-white absolute top-0 left-0 max-lg:text-[10px] max-lg:p-[5px_24px_5px_8px]"
      >
        {{ workshop.kind }}
      </p>
    </div>
    <div class="p-[16px_10px_16px_20px] bg-white">
      <h4
        class="text-lg font-medium text-center max-lg:text-sm tracking-[-0.08em]"
      >
        {{ workshop.title }}
      </h4>
      <div
        class="mt-[17px] text-[11px] leading-5 max-lg:text-[10px] max-lg:leading-[18px]"
      >
        <div
          v-for="(item, i) of workshop.contents"
          :key="i"
          class="flex gap-[20px]"
        >
          <h6 class="min-w-[50px]">{{ item.label }}</h6>
          <p>{{ item.value }}</p>
        </div>
      </div>
    </div>
    <div
      class="bg-[#F9F9F9] border-t bordert-[#DDDDDD] pt-[20px] pb-[10px] px-[20px] max-lg:pt-[10px] max-lg:pb-[5px] max-lg:px-[10px]"
    >
      <div class="flex justify-between">
        <div class="flex items-center gap-[10px]">
          <img
            :src="workshop.user_avatar"
            class="w-[40px] h-[40px] rounded-full"
          />
          <div class="font-bold">
            <p class="text-[8px] font-medium">{{ workshop.user_role }}</p>
            <h6 class="text-[12px] font-medium">{{ workshop.user_name }}</h6>
          </div>
        </div>
        <div class="flex items-center">
          <img :src="workshop.ranking_icon" class="w-[64px] h-auto" />
        </div>
      </div>
      <img :src="workshop.graph" class="w-full h-auto mt-[24px]" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import type { Item } from "../molecules/Workshop.vue";

defineProps<{
  workshop: Item;
}>();
</script>
<style scoped>
.clip-board {
  clip-path: polygon(0 0, 0 100%, calc(100% - 15px) 100%, 100% 0);
}
</style>
