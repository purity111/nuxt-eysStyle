<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  imgUrl?: string;
  title?: string;
  content?: string;
  target?: string;
  isOnlyOne?: boolean;
  isEnd?: boolean;  
}>();
</script>

<template>
  <a
    class="flex justify-start gap-[10px] items-center justify-between pr-[10px] border-b border border-[#DDDDDD]"
    :href="props.target ? props.target : '#'"
  >
    <img
      :src="props.imgUrl"
      class="w-[60px] lg:w-[100px]"
      alt="アコーディオンアイテム"
      loading="lazy"
      decoding="async"
    />
    <div>
      <h5
        class="text-[12px] lg:text-[15px] hiragino-sans pb-[8px] font-medium tracking-[-0.18em]"
      >
        {{ props.title }}
      </h5>
      <p
        class="hiragino-sans text-[#666666] text-[8px] lg:text-[12px] font-medium tracking-[-0.02em]"
      >
        {{ props.content }}
      </p>
    </div>
    <img src="/img/common/arrow.png" class="h-[13px] lg:h-[20px]" alt="arrow" />
  </a>
</template>
