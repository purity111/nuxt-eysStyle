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
  const futureDate = new Date(now.getFullYear(), props.month - 1, props.day, 23, 59); 
  
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
}

calculateTimeDifference();
let intervalId : any;

onMounted(() => {
    intervalId = setInterval(calculateTimeDifference, 1000);
});

onBeforeUnmount(() => {
    if(intervalId) clearInterval(intervalId);
});
</script>

<template>
  <div
    class="flex pl-[26px] py-[10px] rounded-tl-[6px] rounded-tr-[6px] items-center"
  >
    <div class="flex roboto justify-start items-center">
      <h3 class="text-[20px] font-bold italic roboto text-[#FAB6B0] leading-none">
        {{ props.month }}/{{ props.day }}
      </h3>
      <p class="text-[12px] pl-[10px] pr-[6px]">23:59</p>
      <p class="text-[12px]">まで</p>
    </div>
    <p class="roboto text-[12px] pl-[20px] pr-[6px]">残り</p>
    <div class="flex justify-start gap-[3px] items-center">
      <AtomsTimeSnippet :col="'#FAB6B0'" :num="days" :text="'日'" />
      <AtomsTimeSnippet :col="'#FAB6B0'" :num="hours" :text="'時間'" />
      <AtomsTimeSnippet :col="'#FAB6B0'" :num="minutes" :text="'分'" />
      <AtomsTimeSnippet :col="'#FAB6B0'" :num="seconds" :text="'秒'" />
    </div>
  </div>
</template>
