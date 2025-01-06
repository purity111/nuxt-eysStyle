<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  col?: string;
  num?: number;
  text?: string;
}>();
</script>

<template>
  <div class="flex roboto items-center">
    <p class="text-[16px]" :style="{ color: props.col }">{{ props.num }}</p>
    <p class="text-[10px] pl-[2px] hiragino-sans">{{ props.text }}</p>
  </div>
</template>
