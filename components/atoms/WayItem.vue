<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  title?: string;
}>();
</script>

<template>
  <div>
    <h4 class="text-[16px] text-center">{{ props.title }}</h4>
    <img
      class="w-[540px] mr-[-40px]"
      src="/img/pc/cost-bg.avif"
      alt="左側画像"
      loading="lazy"
      decoding="async"
    />
  </div>
</template>
