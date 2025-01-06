<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  logoUrl: string;
  siteCaption?: string;
  siteTitle?: string;
  targetUrl: string;
  isFirst?: boolean;
  isSecond?: boolean;
  bg?: string;
}>();
</script>

<template>
  <a
    class="w-full lg:w-[455px] lg:"
    :href="props.targetUrl"
    :style="{ backgroundColor: props.bg }"
    target="_blank"
  >
    <div
      class="w-full h-[1px] border border-[#DDDDDD] border-t-0"
      v-if="props.isFirst === true"
    />
    <div
      class="w-full h-[1px] border border-[#DDDDDD] border-t-0 hidden lg:block"
      v-if="props.isSecond === true"
    />
    <div
      class="flex items-center justify-between my-[15px] lg:pl-[5px] lg:pr-[20px] lg:my-[18px]"
    >
      <div class="grid place-content-center w-[50%] lg:w-[30%]">
        <img
          class="max-h-[36px] lg:max-h-[40px]"
          :src="props.logoUrl"
          alt="sub-logo"
          loading="lazy"
          decoding="async"
        />
      </div>
      <div
        class="flex items-center justify-between pl-5 pr-[10px] w-[50%] gap-[30px] lg:w-[58%]"
      >
        <div>
          <p class="text-[10px] pb-1">{{ props.siteCaption }}</p>
          <h5 class="text-[13px] tracking-[-0.15em]">{{ props.siteTitle }}</h5>
        </div>
        <img class="w-[6px]" src="/img/common/right-arrow.svg" alt="行き" />
      </div>
    </div>
    <div class="w-full h-[1px] border border-[#DDDDDD] border-t-0" />
  </a>
</template>
