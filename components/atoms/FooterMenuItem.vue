<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  text?: string;
}>();
</script>

<template>
  <div class="flex justify-start gap-[10px]">
    <img
      class="h-[5px] lg:hidden"
      src="/img/common/navigation-right.png"
      alt="arrow"
    />
    <h6
      class="hiragino-sans text-[11px] lg:text-[13px] lg:text-[13px] leading-none tracking-[-0.15em]"
    >
      <span class="hidden lg:inline-block">- </span>{{ props.text }}
    </h6>
  </div>
</template>
