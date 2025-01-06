<script setup lang="ts">
import { defineProps, onBeforeUnmount, onMounted } from "vue";

const props = defineProps<{
  month?: number;
  day?: number;
}>();

const days = ref(0);
const hours = ref(0);
const minutes = ref(0);
const seconds = ref(0);

const calculateTimeDifference = () => {
  const now = new Date();
  const futureDate = new Date(
    now.getFullYear(),
    props.month - 1,
    props.day,
    23,
    59
  );

  if (futureDate < now) {
    futureDate.setFullYear(futureDate.getFullYear() + 1);
  }

  const diffInMs = futureDate.getTime() - now.getTime();

  if (diffInMs > 0) {
    const totalSeconds = Math.floor(diffInMs / 1000);
    days.value = Math.floor(totalSeconds / 86400);
    hours.value = Math.floor((totalSeconds % 86400) / 3600);
    minutes.value = Math.floor((totalSeconds % 3600) / 60);
    seconds.value = totalSeconds % 60;
  } else {
    days.value = hours.value = minutes.value = seconds.value = 0;
  }
};

calculateTimeDifference();
let intervalId: any;

onMounted(() => {
  intervalId = setInterval(calculateTimeDifference, 1000);
});

onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId);
});
</script>

<template>
  <div>
    <img
      src="/img/pc/white-polygon.webp"
      class="w-[180px]"
      alt="残り時間"
      loading="lazy"
      decoding="async"
    />
    <div
      class="absolute top-[27px] left-[50%] -translate-x-1/2 hiragino-sans w-full"
    >
      <p class="text-[14px] text-center">残り</p>
      <div class="flex justify-center gap-[5px] pt-[20px]">
        <div class="flex gap-[5px]">
          <h3
            class="text-[30px] italic text-[#FAB6B0] font-black roboto leading-none"
          >
            {{ days }}
          </h3>
          <p class="text-[14px] leading-[3] pl-[3px]">日</p>
        </div>
        <div class="flex gap-[5px]">
          <h3
            class="text-[30px] italic text-[#FAB6B0] font-black roboto leading-none"
          >
            {{ hours }}
          </h3>
          <p class="text-[14px] leading-[3] pl-[3px]">時間</p>
        </div>
      </div>
      <div class="flex justify-center gap-[4px]">
        <div class="flex gap-[4px]">
          <h3
            class="text-[30px] italic text-[#FAB6B0] font-black roboto leading-none"
          >
            {{ minutes }}
          </h3>
          <p class="text-[14px] leading-[3] pl-[3px]">分</p>
        </div>
        <div class="flex gap-[4px]">
          <h3
            class="text-[30px] italic text-[#FAB6B0] font-black roboto leading-none"
          >
            {{ seconds }}
          </h3>
          <p class="text-[14px] leading-[3] pl-[3px]">秒</p>
        </div>
      </div>
    </div>
  </div>
</template>
