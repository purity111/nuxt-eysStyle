<script setup lang="ts">
import { defineProps, popScopeId } from "vue";

const props = defineProps<{
  icon?: string;
  price?: number;
  link?: string;
  text?: string;
}>();
</script>

<template>
  <a class="grid py-[10px] bg-black" :href="props.link">
    <div class="flex items-center">
      <img
        class="px-[22px] h-[19px] lg:h-[26px]"
        :src="props.icon"
        alt="登録アイコン"
        loading="lazy"
        decoding="async"
      />
      <p
        class="text-white hiragino-sans text-[12px] lg:text-[18px] leading-0"
        v-if="!props.text"
      >
        メンバー登録して{{ props.price }}円GET
      </p>
      <p
        class="text-white hiragino-sans text-[12px] lg:text-[18px] leading-0"
        v-if="props.text"
      >
        {{ text }}
      </p>
    </div>
  </a>
</template>
