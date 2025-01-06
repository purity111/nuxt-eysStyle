<template>
  <div class="mt-[110px]">
    <img
      class="w-[150px] m-auto hidden lg:block pb-[40px]"
      src="/img/common/system-art.png"
      alt="アートタイトル"
      loading="lazy"
      decoding="async"
    />
    <h2 class="text-center text-[18px] lg:text-[32px]">
      “本気度”自由自在！<br />
      様々な通い方をご用意しています
    </h2>
    <div
      class="block lg:flex mt-[50px] lg:pt-[100px] lg:w-[1000px] lg:m-auto justify-between"
    >
      <MoleculesSystemItem
        :num="'01'"
        :titleCaption="'色々なコース＆講師を試したい方は'"
        :title="'オールフリー制'"
        :imgUrl="'/img/common/system1.webp'"
        :tblTitle="'チケット制で、<br>色々なコースを受講'"
        :tblData="{
          course: [10, 30, 50, 100],
          cost: [40000, 114000, 180000, 350000],
        }"
        class="mb-[30px] lg:m-0"
      />
      <div class="flex px-[10px] lg:px-0">
        <MoleculesSystemItem
          :num="'02'"
          :titleCaption="'1つのコースをお得に受講したい方は'"
          :title="'専科制'"
          :imgUrl="'/img/common/system2.webp'"
          :tblTitle="'月謝制で、<br>お得に受講！'"
          :tblData="{
            course: [2, 4, 8, 12],
            cost: [8000, 16000, 32000, 48000],
          }"
          class="mb-[30px] lg:mb-0 lg:mr-[20px]"
        />
        <MoleculesSystemItem
          :num="'03'"
          :titleCaption="'まずはお試しで参加したい方は'"
          :title="'セメスター制'"
          :imgUrl="'/img/common/system3.webp'"
          :tblTitle="'３〜４ヶ月の期間で、<br>お試し受講！'"
          :tblData="{
            course: [2, 4, 8, 12],
            cost: [8000, 16000, 32000, 48000],
          }"
          class="mb-[30px] lg:mb-0"
        />
      </div>
    </div>
    <img
      class="lg:hidden h-[40px] m-auto"
      src="/img/common/union-grey.svg"
      alt="ユニオン"
    />
    <img
      class="hidden lg:block lg:pt-[20px] lg:pb-[10px] m-auto"
      src="/img/common/union-grey-pc.svg"
      alt="ユニオン"
    />
    <h4
      class="text-center text-[16px] lg:text-[28px] pb-[55px] lg:pb-[90px] mt-[20px] font-medium"
    >
      どの通い方でも、<br />
      オンライン/オフライン自由自在！
    </h4>
  </div>
</template>
