<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  imgUrl?: string;
  text?: string;
  fSize?: number;
  height?: number;
  width?: number;
  distance?: number;
}>();
</script>

<template>
  <div>
    <img
      :src="props.imgUrl"
      :style="{ height: props.height + 'px', width: props.width + 'px' }"
      class="m-auto"
      alt="アートタイトル"
      loading="lazy"
      decoding="async"
    />
    <h4
      class="text-center leading-[1.8] tracking-[-0.06em] font-medium"
      :style="{
        marginTop: props.distance + 'px',
        fontSize: props.fSize + 'px',
      }"
      v-html="props.text"
    ></h4>
  </div>
</template>
