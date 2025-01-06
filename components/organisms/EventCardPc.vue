<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  price?: number;
  mon?: number;
  day?: number;
}>();
</script>

<template>
  <div class="relative hidden lg:flex m-auto w-[max-content]">
    <img
      class="h-[300px] m-auto mr-[-40px]"
      src="/img/pc/cost-bg.avif"
      alt="プレゼント"
      loading="lazy"
      decoding="async"
    />
    <img
      class="h-[300px] m-auto ml-[-40px]"
      src="/img/pc/cost-photo.avif"
      alt="プレゼント"
      loading="lazy"
      decoding="async"
    />
    <div class="absolute top-[6px] left-[20px]">
      <h5 class="text-[20px] pb-[20px] tracking-[0.3em]">
        今だけ、新規登録キャンペーン中！
      </h5>
      <p class="text-white text-[16px]">
        スクールの入会金に充当できる、2000円相当
      </p>
      <div class="flex justify-start mt-[10px] mb-[20px]">
        <AtomsPriceLogo
          :icon="'/img/common/circle-logo.png'"
          class="w-[130px] h-[130px] mr-[10px]"
          :price="props.price"
        />
        <AtomsPricePresent :price="props.price" />
      </div>
      <AtomsPriceBtn
        :icon="'/img/common/register-icon.svg'"
        :price="props.price"
        class="w-[420px] h-[50px] place-content-center"
      />
    </div>
    <div class="polygons">
      <AtomsTimePolygon
        class="absolute bottom-[10px] right-[120px]"
        :month="props.mon"
        :day="props.day"
      />
      <AtomsTargetPolygon
        class="absolute top-[10px] right-[10px]"
        :mon="props.mon"
        :day="props.day"
      />
    </div>
  </div>
</template>

<style scoped>
.shadow {
  box-shadow: 0 10px 6px rgb(0, 0, 0, 0.15);
}
</style>
