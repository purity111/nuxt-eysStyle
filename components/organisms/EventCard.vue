<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  price?: number;
  mon?: number;
  day?: number;
}>();
</script>

<template>
  <div class="mx-[10px] lg:hidden mt-[-210px]">
    <MoleculesTimeBar :month="props.mon" :day="props.day" class="bg-white" />
    <div class="shadow bg-[url('/img/sp/register-bg.avif')] p-[10px]">
      <div class="relative z-20">
        <p class="text-white text-[13px] text-center tracking-normal">
          ＼ 今だけ、新規登録キャンペーン中！ ／
        </p>
        <div class="flex items-center justify-center gap-[10px] py-[10px]">
          <AtomsPriceLogo
            :icon="'/img/common/circle-logo.png'"
            class="w-[82px] h-[82px]"
            :price="props.price"
          />
          <div>
            <p
              class="text-[9px] hiragino-sans roboto text-white text-center tracking-[-0.1em]"
            >
              スクールの入会金に充当できる{{ props.price }}円相当
            </p>
            <AtomsPricePresent :price="props.price" />
          </div>
        </div>
        <AtomsPriceBtn
          :icon="'/img/common/register-icon.svg'"
          :price="props.price"
          class="w-[250px] h-[36px] m-auto"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.shadow {
  box-shadow: 0 10px 6px rgb(0, 0, 0, 0.15);
}
</style>
