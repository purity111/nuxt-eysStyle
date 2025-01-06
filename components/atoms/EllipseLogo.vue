<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  imgUrl?: string;
}>();
</script>

<template>
  <div class="relative">
    <img
      src="/img/common/ellipse.webp"
      class="m-auto w-[126px] lg:w-[200px]"
      alt="スクールロゴ"
      loading="lazy"
      decoding="async"
    />
    <img
      :src="props.imgUrl"
      class="absolute left-[50%] top-[50%] -translate-x-1/2 -translate-y-1/2 w-[85px] lg:w-[125px]"
      alt="スクールロゴ"
      loading="lazy"
      decoding="async"
    />
  </div>
</template>
