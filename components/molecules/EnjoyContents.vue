<template>
  <div class="relative top-0 left-[50%] -translate-x-1/2 w-full">
    <div class="pt-[35px] lg:pt-[60px]">
      <img
        class="m-auto h-[40px] lg:h-[65px]"
        src="/img/common/about-art.png"
        alt="私たちについて"
        loading="lazy"
        decoding="async"
      />
      <h4
        class="text-[18px] lg:text-[40px] leading-[2] pt-[22px] lg:pt-[50px] text-center leading-none pb-[12px] lg:pb-[26px]"
      >
        Enjoy Your Life
      </h4>
      <h4
        class="text-[18px] lg:text-[40px] leading-[2] tracking-[-0.1em] text-center leading-none"
      >
        文化的・芸術的なライフスタイルとは
      </h4>
    </div>
    <div
      class="text-[13px] lg:text-[16px] pt-[40px] lg:pt-[100px] tracking-[-0.08em] text-center leading-[2]"
    >
      <p class="pb-[30px] lg:pb-[50px]">
        誰もが望む、<br />
        経済的にも精神的にも、<br />
        本当の意味で豊かなライフスタイル。
      </p>
      <p class="pb-[30px] lg:pb-[50px]">
        その実現のためには、<br />
        何が必要なのでしょうか？
      </p>
      <p class="pb-[30px] lg:pb-[50px]">
        私たちEYS-STYLEは、<br />
        <span class="lg:hidden">
          その「答」は <br />
          “学び” と “コミュニティ” にあると考えます。
        </span>
        <span class="hidden lg:block">
          その「答」は “学び” と “コミュニティ” にあると考えます。
        </span>
      </p>
      <p class="pb-[30px] lg:pb-[50px]">
        人生100年時代、<br />
        常に学び続け自分をアップデートし、<br />
        確固たるキャリアと資産の土台を築くこと。<br />
        一方で、<br />
        家族・子供・友人関係といった、<br />
        人間本来の豊かさを育む<br />
        コミュニティを大切にすること。
      </p>
      <p class="pb-[30px] lg:pb-[50px]">
        この２つが揃ってこそ、<br />
        本当の意味で豊かな、 <br />
        <span class="lg:hidden">
          文化的・芸術的なライフスタイルが<br />
          実現するのではないでしょうか。
        </span>
        <span class="hidden lg:block">
          文化的・芸術的なライフスタイルが実現するのではないでしょうか。
        </span>
      </p>
      <p class="pb-[30px] lg:pb-[50px]">Enjoy Your Life</p>
      <p class="pb-[30px] lg:pb-[50px]">
        <span class="lg:hidden">
          あなたの人生をより彩り豊かで<br />
          満たされたものにするために。<br />
        </span>
        <span class="hidden lg:block">
          あなたの人生をより彩り豊かで 満たされたものにするために。<br />
        </span>
        <span class="lg:hidden">
          EYS-STYLEには、<br />
          そこに至る「答」があります。
        </span>
        <span class="hidden lg:block">
          EYS-STYLEには、そこに至る「答」があります。
        </span>
      </p>
    </div>
    <div class="pt-[70px]">
      <img
        class="w-[108px] lg:w-[175px] m-auto"
        src="/img/common/main-logo.png"
        alt="ロゴ"
        loading="lazy"
        decoding="async"
      />
      <div
        class="flex items-center justify-between lg:justify-center lg:gap-[80px] px-[10px] pt-[40px] lg:pt-[50px]"
      >
        <AtomsStyleItem
          :title="'“学び”'"
          :content="'キャリア形成、資産形成、<br>文化や芸術的な学びまで。<br>一生涯にわたるリカレント教育を提供。'"
          :iconUrl="'/img/sp/study-icon.svg'"
          class="lg:hidden"
        />
        <AtomsStyleItem
          :title="'“学び”'"
          :content="'キャリア形成、資産形成、文化や芸術的な学びまで。<br>経済的豊かさと精神的豊かさを手に入れるために、<br>一生涯にわたるリカレント教育を提供。'"
          :iconUrl="'/img/pc/study.webp'"
          class="hidden lg:flex"
        />
        <img
          class="w-[32px] h-[32px] lg:w-[70px] lg:h-[70px] mr-[25px] lg:mr-0"
          src="/img/common/plus.png"
          alt="プラス"
          loading="lazy"
          decoding="async"
        />
        <AtomsStyleItem
          :title="'“コミュニティ”'"
          :content="'安定した資産と、<br>文化的・芸術的ライフスタイル<br>など本質的なQOL実現へ。'"
          :iconUrl="'/img/sp/community-icon.svg'"
          class="lg:hidden"
        />
        <AtomsStyleItem
          :title="'“コミュニティ”'"
          :content="'安定した資産と、それをベースにした<br>文化的・芸術的ライフスタイルを実現するだけでなく、<br>家族・子供・友人など本質的なQOL実現へ。'"
          :iconUrl="'/img/pc/community.webp'"
          class="hidden lg:flex"
        />
      </div>
      <img
        class="h-[30px] lg:h-[70px] mt-[30px] mb-[20px] lg:h-[70px] lg:mt-[45px] lg:mb-[25px] m-auto"
        src="/img/common/union.png"
        alt="ロゴ"
        loading="lazy"
        decoding="async"
      />
      <h5 class="text-center text-[14px] lg:text-[28px] font-medium">
        “学び”と“コミュニティ”で、<br />
        真に文化的・芸術的なライフスタイルを。<br />
        EYS-STYLEなら実現できます。
      </h5>
      <img
        class="m-auto mt-[30px] mb-[25px] w-[185px] lg:w-[300px] lg:mt-[55px] lg:mb-[50px]"
        src="/img/common/brand.webp"
        alt="ロゴ"
        loading="lazy"
        decoding="async"
      />
      <h4 class="text-center text-[22px] lg:text-[40px] font-medium">
        さあ、あなたも
      </h4>
      <h4
        class="text-center text-[22px] lg:text-[40px] tracking-[0.1em] font-medium"
      >
        Enjoy Your Life
      </h4>
    </div>
  </div>
</template>
