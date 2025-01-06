<template>
  <div
    class="w-full mt-[165px] max-lg:mt-[71px] max-lg:max-w-[375px] max-lg:mx-auto overflow-hidden bg-contain bg-no-repeat bg-top"
  >
    <img
      src="/img/common/community-title.svg"
      alt="community"
      class="w-[443px] mx-auto max-lg:w-[275px]"
    />
    <h5
      class="mt-[40px] text-[40px] font-medium text-center leading-[70px] max-lg:text-lg max-lg:mt-[15px]"
    >
      キャリア形成・資産形成に留まらない、<br />すべての人の<br
        class="lg:hidden"
      />セカンドコミュニティへ
    </h5>
    <div class="relative">
      <picture>
        <source
          media="(max-width: 1023px)"
          srcset="/img/sp/community-imgs.avif"
        />
        <img
          src="/img/pc/community-images.avif"
          alt="community"
          class="absolute min-w-[1920px] top-0 left-1/2 -translate-x-1/2 h-auto max-lg:min-w-[375px]"
        />
      </picture>
      <p
        class="relative text-center font-medium text-base pt-[108px] pb-[233px] leading-[40px] max-lg:text-[13px] max-lg:pt-[36px] max-lg:leading-[26px] max-lg:pb-[91px]"
      >
        EYS-STYLEは創業以来、<br />
        多くの会員様の出会いを<br />
        プロデュースしてきました。<br />
        <br />
        出会いは、<br />
        ビジネス上のアライアンスから、<br />
        結婚したカップルまで、<br />
        実に様々です。<br />
        <br />
        Enjoy Your Life の<br />
        もうひとつの大切な要素、<br />
        それが“コミュニティ”<br />
        <br />
        ここには、<br />
        出会いを生み出す<br />
        “仕掛け”と“文化”があります。
      </p>
    </div>
    <div class="pt-[20px] relative">
      <h3
        class="text-[30px] text-center font-medium max-lg:text-lg tracking-[-0.2em]"
      >
        繋がりとコミュニケーションを促進する、<br />コミュニティの場作り
      </h3>
      <img
        src="/img/pc/community-logo.svg"
        alt="community"
        class="w-[200px] mx-auto mt-[77px] max-lg:w-[103px] max-lg:mt-[15px]"
      />
      <div
        class="flex justify-between w-full max-w-[1000px] mx-auto max-lg:px-[10px] mt-[60px] max-lg:mt-[23px]"
      >
        <img
          src="/img/common/iPhone1.avif"
          alt="community"
          class="w-[300px] h-auto max-lg:w-[114px]"
        />
        <img
          src="/img/common/iPhone2.avif"
          alt="community"
          class="w-[300px] h-auto max-lg:w-[114px]"
        />
        <img
          src="/img/common/iPhone3.avif"
          alt="community"
          class="w-[300px] h-auto max-lg:w-[114px]"
        />
      </div>
    </div>
    <div class="pt-[153px] max-lg:pt-[71px]">
      <h3 class="text-[32px] font-medium text-center max-lg:text-lg">
        皆さんの声
      </h3>
      <div
        class="w-full mt-[26px] max-lg:mt-[30px] overflow-hidden pb-[100px] max-lg:pb-[50px]"
      >
        <MoleculesSaying v-if="datas.length > 0" :sayings="datas" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, onMounted } from "vue";
const datas = ref([]);

onMounted(async () => {
  try {
    const response = await fetch("/data/sayings.json");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    const data = await response.json();
    datas.value = data;
  } catch (error) {
    console.error("Fetch error:", error);
  }
});
</script>
