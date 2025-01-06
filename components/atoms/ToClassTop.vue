<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  text?: string;
}>();
</script>

<template>
  <div class="relative bg-black grid place-content-center">
    <p class="text-center text-white text-[10px] lg:text-[15px]">
      {{ props.text }}
    </p>
    <img
      src="/img/common/right-arrow.png"
      class="absolute top-[50%] -translate-y-1/2 right-[4%] w-[8px] lg:w-[12px]"
      alt="矢印"
    />
  </div>
</template>