<template>
  <div class="w-[320px] max-lg:w-[260px]">
    <h5
      v-html="item.title"
      class="text-lg p-[25px_46px_43px] font-medium text-center bg-[url('/img/pc/bubble.png')] bg-no-repeat bg-center bg-contain drop-shadow-xl max-lg:text-sm max-lg:p-[20px_40px_43px] relative z-30"
    ></h5>
    <div class="w-full border border-[#DDDDDD] bg-white mt-[-10px] z-20 relative">
      <img :src="item.banner" :alt="item.user_name" class="w-full h-auto" />
      <h6
        class="text-center text-lg font-semibold pt-[17px] max-lg:text-sm max-lg:mt-[4px]"
      >
        {{ item.user_name }}<span class="text-xs max-lg:text-[11px]">さん</span>
      </h6>
      <div class="w-full pt-[17px] px-[20px] pb-[20px] max-lg:px-[10px]">
        <img
          src="/img/common/quotes.png"
          width="40"
          height="auto"
          alt="saying"
          class="w-[40px] h-auto mr-auto max-lg:w-[26px]"
        />
        <p
          v-html="item.description"
          class="text-[11px] w-full px-[20px] max-lg:text-[10px] max-lg:px-[10px]"
        ></p>
        <img
          src="/img/common/quotes.png"
          width="40"
          height="auto"
          alt="saying"
          class="w-[40px] h-auto ml-auto max-lg:w-[26px] rotate-180"
        />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
export interface Saying {
  title: string;
  banner: string;
  user_name: string;
  description: string;
}
defineProps<{
  item: Saying;
}>();
</script>
