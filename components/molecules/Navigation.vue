<script setup lang="ts">
import { ref } from "vue";

const showLearnMenu = ref(false);
const showCommunityMenu = ref(false);
</script>

<template>
  <div
    class="absolute w-full"
    @mouseleave="(showCommunityMenu = false), (showLearnMenu = false)"
  >
    <div class="bg-[rgba(255,255,255,0.8)]">
      <div class="flex lg:m-auto lg:w-[1000px]">
        <AtomsMenu
          :feature="'EYS-STYLEが提供する'"
          :title="'“学び”'"
          class="border-r-0"
          @mouseenter="(showLearnMenu = true), (showCommunityMenu = false)"
        />
        <AtomsMenu
          :feature="'EYS-STYLEが提供する'"
          :title="'“コミュニティ”'"
          @mouseenter="(showCommunityMenu = true), (showLearnMenu = false)"
        />
      </div>
    </div>
    <nav
      v-if="showLearnMenu"
      class="bg-white bShadow py-[15px] px-[10px] lg:p-[30px] border border-t-0 border-[#DDDDDD] lg:flex lg:flex-wrap lg:w-[1000px] lg:m-auto lg:justify-between"
    >
      <AtomsChildMenu
        :logo-url="'/img/common/logo-eys.svg'"
        :siteCaption="'全32種の豊富なレッスン'"
        :siteTitle="'大人の音楽教室'"
        :targetUrl="'#'"
        :isFirst="true"
        :bg="'white'"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/logo-wine1.png'"
        :siteCaption="'どこよりも初心者に優しい'"
        :siteTitle="'ワインスクール'"
        :targetUrl="'#'"
        :isSecond="true"
        :bg="'white'"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :bg="'white'"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :bg="'white'"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :bg="'white'"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/temp-logo.png'"
        :siteTitle="'下層サイト'"
        :targetUrl="'#'"
        :bg="'white'"
      />
    </nav>
    <!--menu1-->
    <nav
      v-if="showCommunityMenu"
      class="bg-white bShadow py-[15px] px-[10px] lg:p-[30px] border border-t-0 border-[#DDDDDD] lg:flex lg:flex-wrap lg:w-[1000px] lg:m-auto lg:justify-between"
    >
      <AtomsChildMenu
        :logo-url="'/img/common/2nd-logo1.png'"
        :siteCaption="'出会いを生み出す“仕掛け”と“文化”'"
        :siteTitle="'セカンドコミュニティ'"
        :targetUrl="'#'"
        :bg="'white'"
        :isFirst="true"
      />
      <AtomsChildMenu
        :logo-url="'/img/common/woman-community.png'"
        :siteCaption="'スクールで恋して結婚する新しいカタチ'"
        :siteTitle="'恋活・婚活コミュニティ'"
        :targetUrl="'#'"
        :bg="'white'"
        :isSecond="true"
      />
    </nav>
  </div>
</template>
