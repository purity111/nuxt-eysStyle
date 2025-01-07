<script setup lang="ts">
import { defineProps, popScopeId } from "vue";

const props = defineProps<{
  icon?: string;
  link?: string;
  text?: string;
}>();
</script>

<template>
  <a class="grid py-[10px] bg-black" :href="props.link">
    <div class="flex items-center">
      <img
        class="px-[22px] h-[14px] lg:h-[20px]"
        :src="props.icon"
        alt="登録アイコン"
        loading="lazy"
        decoding="async"
      />
      <p class="text-white hiragino-sans text-[14px] lg:text-[18px] leading-0">
        {{ text }}
      </p>
    </div>
  </a>
</template>
