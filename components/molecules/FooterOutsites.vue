<template>
  <div
    class="bg-black pt-[55px] pb-[115px] text-white lg:text-[#777777] lg:pt-[100px] lg:pb-[170px] lg:m-auto"
  >
    <img
      class="h-[60px] m-auto"
      src="/img/common/EYS-footer-logo.svg"
      alt="フッターロゴ"
      loading="lazy"
      decoding="async"
    />
    <div class="flex flex-wrap mb-[50px] lg:mb-[75px] mt-[60px] px-[40px] lg:w-[1000px] lg:m-auto lg:mt-[90px] lg:justify-between">
      <div class="w-[50%] lg:w-[25%] mb-[40px]">
        <h5 class="text-[12px] pb-[20px]">フッタリンク大</h5>
        <div>
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" />
        </div>
      </div>
      <div class="w-[50%] lg:w-[25%] mb-[40px]">
        <h5 class="text-[12px] pb-[20px]">フッタリンク大</h5>
        <div>
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" />
        </div>
      </div>
      <div class="w-[50%] lg:w-[25%]">
        <h5 class="text-[12px] pb-[20px]">フッタリンク大</h5>
        <div>
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" />
        </div>
      </div>
      <div class="w-[50%] lg:w-[25%]">
        <h5 class="text-[12px] pb-[20px]">フッタリンク大</h5>
        <div>
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" class="mb-[15px]" />
          <AtomsFooterMenuItem :text="'フッタリンク小'" />
        </div>
      </div>
    </div>
    <p class="text-center text-[8px] lg:text-[10px] tracking-[0.16em]">
      ©2nd Community inc. All rights reserved.
    </p>
  </div>
</template>
