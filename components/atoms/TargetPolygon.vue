<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  mon?: number;
  day?: number;
}>();
</script>

<template>
  <div class="grid place-content-center">
    <div class="relative">
      <img
        src="/img/pc/pink-polygon.webp"
        class="h-[180px]"
        alt="ターゲット日"
        loading="lazy"
        decoding="async"
      />
      <div class="absolute top-0 w-full h-full pt-[40px] pb-[30px] px-[42px]">
        <h1
          class="text-left text-white leading-none font-bold text-[40px] roboto italic"
        >
          <span
            class="pl-[10px] inline-block"
            v-if="props.mon.toString().length === 1"
          ></span
          >{{ props.mon }}
        </h1>
        <div class="bg-white h-[4px] w-[100px] rotate-[-45deg]"></div>
        <h1
          class="text-right text-white leading-none font-bold text-[40px] roboto italic"
        >
          {{ props.day }}
        </h1>

        <p class="text-white text-center hiragino-sans pt-[10px] text-[14px]">
          まで
        </p>
      </div>
    </div>
  </div>
</template>
