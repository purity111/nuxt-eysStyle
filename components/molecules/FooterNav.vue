<template>
  <div class="">
    <div
      class="border border-l-0 border-r-0 mx-[10px] border-[#DDDDDD] py-[20px] lg:py-[25px] lg:w-[1000px] lg:m-auto text-center text-[18px] lg:text-[20px] font-medium lg:border-b-0"
    >
      学び
    </div>
    <nav
      class="py-[15px] px-[10px] lg:p-[30px] lg:flex lg:flex-wrap lg:w-[1000px] lg:m-auto lg:justify-between lg:pt-0"
    >
      <AtomsFooterChildMenu
        :logo-url="'/img/common/logo-eys.svg'"
        :siteCaption="'全32種の豊富なレッスン'"
        :siteTitle="'大人の音楽教室'"
        :targetUrl="'#'"
        :isFirst="true"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/logo-wine1.png'"
        :siteCaption="'どこよりも初心者に優しい'"
        :siteTitle="'ワインスクール'"
        :targetUrl="'#'"
        :isSecond="true"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :isViceEnd="true"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :isEnd="true"
        class="border-b-0"
      />
    </nav>
    <div
      class="border border-l-0 border-r-0 mx-[10px] border-[#DDDDDD] py-[20px] lg:py-[25px] lg:w-[1000px] lg:m-auto text-center text-[18px] lg:text-[20px] font-medium lg:border-b-0 tracking-[-0.2em] mt-[20px]"
    >
      コミュニティ
    </div>
    <nav
      class="px-[10px] lg:p-[30px] lg:flex lg:flex-wrap lg:w-[1000px] lg:m-auto lg:justify-between lg:pt-0 pb-[55px] lg:pb-[96px]"
    >
      <AtomsFooterChildMenu
        :logo-url="'/img/common/2nd-logo1.png'"
        :siteCaption="'出会いを生み出す“仕掛け”と“文化”'"
        :siteTitle="'セカンドコミュニティ'"
        :targetUrl="'#'"
        :isFirst="true"
      />
      <AtomsFooterChildMenu
        :logo-url="'/img/common/woman-community.png'"
        :siteCaption="'スクールで恋して結婚する新しいカタチ'"
        :siteTitle="'恋活・婚活コミュニティ'"
        :targetUrl="'#'"
        :isSecond="true"
      />
    </nav>
  </div>
</template>
