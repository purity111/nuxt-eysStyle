<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  text?: string;
}>();
</script>

<template>
  <div class="grid place-content-center bg-black">
    <h5 class="text-center">
      {{ props.text }}
    </h5>
  </div>
</template>
