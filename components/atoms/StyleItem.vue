<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  title?: string;
  content?: string;
  iconUrl?: string;
}>();
</script>

<template>
  <div
    class="flex flex-col justify-between items-center h-[180px] lg:h-[400px]"
  >
    <h4 class="text-center text-[16px] lg:text-[32px] tracking-normal">
      {{ title }}
    </h4>
    <img
      :src="props.iconUrl"
      class="m-auto h-[68px] lg:h-[213px]"
      alt="アイコン"
      loading="lazy"
      decoding="async"
    />
    <p
      class="text-center tracking-[-0.08em] leading-[1.8] text-[10px] lg:text-[13px] tracking-[-0.14em]"
      v-html="props.content"
    ></p>
  </div>
</template>
