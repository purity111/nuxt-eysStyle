<template>
  <div class="lg:w-[1000px] m-auto">
    <AtomsArtTitle
      :imgUrl="'/img/common/lesson-art.png'"
      :text="'リアルでもオンラインでも<br>EYS-STYLE'"
      :height="38"
      :fSize="32"
      :distance="40"
      class="hidden lg:block"
    />
    <AtomsArtTitle
      :imgUrl="'/img/common/lesson-art.png'"
      :text="'リアルでもオンラインでも<br>EYS-STYLE'"
      :height="30"
      :fSize="18"
      :distance="20"
      class="lg:hidden"
    />

    <div
      class="flex justify-between mt-[40px] lg:mt-[70px] pl-[20px] pr-[10px] lg:pl-0 lg:pr-0"
    >
      <div>
        <h3 class="text-[16px] lg:hidden pt-[15px] tracking-[-0.1em]">
          オンラインで、<br />
          全国どこからでも<br />
          レッスン可能！
        </h3>
        <h3 class="text-[28px] hidden lg:block pt-[25px] tracking-[-0.12em]">
          オンラインで、<br />
          全国どこからでも レッスン可能！
        </h3>
        <p
          class="hiragino-sans hidden lg:block text-[13px] pt-[30px] tracking-[-0.18em]"
        >
          お持ちのスマートフォン・タブレット・PCから、<br />
          いつでもどこでもカンタン３ステップでレッスンが受講できます。
        </p>
      </div>
      <img
        class="w-[195px] lg:w-[610px]"
        src="/img/common/Laptop.avif"
        alt="ラップトップ"
        loading="lazy"
        decoding="async"
      />
    </div>
    <p
      class="hiragino-sans text-[10px] mt-[13px] lg:hidden pl-[20px] pr-[10px] tracking-[-0.18em]"
    >
      お持ちのスマートフォン・タブレット・PCから、いつでもどこでも<br />
      カンタン３ステップでレッスンが受講できます。
    </p>

    <div
      class="flex justify-between mt-[40px] lg:mt-[70px] pr-[20px] lg:pl-0 lg:pr-0"
    >
      <img
        class="hidden lg:block w-[630px]"
        src="/img/pc/lg-sm.avif"
        alt="オフィス"
        loading="lazy"
        decoding="async"
      />
      <img
        class="w-[175px] ml-[-4px] lg:hidden"
        src="/img/sp/lg-sm-sp.webp"
        alt="オフィス"
        loading="lazy"
        decoding="async"
      />
      <div>
        <h3
          class="text-[16px] text-right lg:hidden pt-[15px] pb-[25px] tracking-[-0.15em]"
        >
          オフラインでも、<br />
          駅チカのおしゃれな<br />
          コミュニティースペース<br />
          をご用意！
        </h3>
        <h3
          class="text-[28px] hidden lg:block text-right pt-[25px] pb-[30px] text-right tracking-[-0.18em] font-medium"
        >
          オフラインでも、<br />
          駅チカのおしゃれな<br />
          コミュニティースペースをご用意！<br />
        </h3>
        <p
          class="hidden lg:block text-[13px] text-right tracking-[-0.12em] hiragino-sans"
        >
          EYS-STYLEのスタジオは全国●ヶ所、さらに続々拡大中！<br />
          すべて駅チカに立地した通いやすい環境です。
        </p>
        <p
          class="lg:hidden text-[10px] text-right tracking-[-0.15em] hiragino-sans"
        >
          EYS-STYLEのスタジオは全国●ヶ所、<br />
          さらに続々拡大中！<br />
          すべて駅チカに立地した通いやすい環境です。<br />
        </p>
      </div>
    </div>
  </div>
</template>
