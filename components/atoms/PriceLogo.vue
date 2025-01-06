<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  icon?: string;
  price?: number;
}>();
</script>

<template>
  <div class="grid place-content-center bg-white rounded-full">
    <div>
      <img
        class="px-[22px] mb-[8px] h-[40px] lg:h-[60px]"
        :src="props.icon"
        alt="サークルロゴ"
        loading="lazy"
        decoding="async"
      />
      <p
        class="text-[#98CAF5] text-center leading-none italic roboto font-bold text-[14px] lg:text-[22px]"
      >
        {{ props.price?.toLocaleString() }}
      </p>
    </div>
  </div>
</template>
