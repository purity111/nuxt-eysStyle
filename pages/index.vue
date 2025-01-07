<template>
  <div class="relative">
    <OrganismsHeaderSection />
    <div ref="section0">
      <LazyOrganismsEventCard :mon="1" :day="30" :price="2000" v-if="show0" />
      <LazyOrganismsEventCardPc
        :mon="1"
        :day="30"
        :price="2000"
        class="mt-[-120px]"
        v-if="show0"
      />
      <LazyOrganismsAbout v-if="show0" />
    </div>
    <div
      class="bg-[url('/img/sp/school-community-sp.avif')] lg:bg-[url('/img/pc/school-community.avif')] schoolCommunity-bg"
    >
      <div class="">
        <AtomsArtTitle
          :height="40"
          :width="197"
          :distance="30"
          :fSize="18"
          :imgUrl="'/img/common/school-art.webp'"
          :text="'EYS-STYLEが運営する<br>Enjoy Your Life 実現のためのスクール'"
          class="pt-[65px] pb-[45px] lg:hidden"
        />
        <AtomsArtTitle
          :height="62"
          :width="307"
          :distance="42"
          :fSize="40"
          :imgUrl="'/img/common/school-art.webp'"
          :text="'EYS-STYLEが運営する<br>Enjoy Your Life 実現のためのスクール'"
          class="pt-[160px] pb-[75px] hidden lg:block"
        />
      </div>
      <div ref="section1">
        <LazyOrganismsSchool v-if="show1" />
        <MoleculesLesson
          class="mt-[50px] lg:mt-[70px] lg:mt-[90px]"
          v-if="show1"
        />
        <LazyOrganismsAccordion
          :parents="accordionDatas"
          class="mt-[40px] mx-[10px] lg:m-auto lg:w-[1000px]"
          v-if="show1"
        />
      </div>
      <img
        class="w-[152px] h-[43px] m-auto hidden lg:block pb-[40px] pt-[110px]"
        src="/img/common/system-art.png"
        alt="アートタイトル"
        loading="lazy"
        decoding="async"
      />
      <div ref="section2">
        <LazyOrganismsSystem v-if="show2" />
        <LazyOrganismsCourse v-if="show2" />
      </div>
      <div
        class="w-full mt-[165px] max-lg:mt-[71px] max-lg:max-w-[375px] max-lg:mx-auto overflow-hidden"
      >
        <img
          src="/img/common/community-title.svg"
          alt="community"
          class="w-[274px] h-[54px] lg:w-[443px] lg:h-[87px] mx-auto"
        />
        <div ref="section3">
          <LazyOrganismsCommunity v-if="show3" />
        </div>
      </div>
    </div>
    <footer class="bg-[#F9F9F9]" ref="footer">
      <img
        class="w-[118px] m-auto pt-[30px] pb-[50px] lg:w[175px] lg:pt-[55px] lg:pb-[80px]"
        src="/img/common/main-logo.png"
        alt="フッターロゴ"
        loading="lazy"
        decoding="async"
      />
      <div v-if="showFooter">
        <LazyMoleculesFooterNav />
        <LazyMoleculesFooterOutsites />
      </div>
    </footer>
    <LazyMoleculesToTop class="w-full px-[10px] bottom-[5px] fixed m-auto z-50 lg:bg-white py-[5px]" />
  </div>
</template>

<script setup lang="ts">
import "./style/global.css";
import { ref, onMounted } from "vue";

const accordionDatas = ref([]);

const show0 = ref(false);
const show1 = ref(false);
const show2 = ref(false);
const show3 = ref(false);
const showFooter = ref(false);

const section0 = ref(null);
const section1 = ref(null);
const section2 = ref(null);
const section3 = ref(null);
const footer = ref(null);

onMounted(async () => {
  createObserver(section0.value, (entries) => {
    if (entries[0].isIntersecting) {
      show0.value = true;
    }
  });
  createObserver(section1.value, (entries) => {
    if (entries[0].isIntersecting) {
      show1.value = true;
    }
  });
  createObserver(section2.value, (entries) => {
    if (entries[0].isIntersecting) {
      show2.value = true;
    }
  });
  createObserver(section3.value, (entries) => {
    if (entries[0].isIntersecting) {
      show3.value = true;
    }
  });
  createObserver(footer.value, (entries) => {
    if (entries[0].isIntersecting) {
      showFooter.value = true;
    }
  });

  try {
    const response = await fetch("/data/AccordionData.json");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    accordionDatas.value = await response.json();
  } catch (error) {
    console.error("Fetch error:", error);
  }
});
</script>

<style scoped>
@media (min-width: 376px) {
  .schoolCommunity-bg {
    background-size: cover;
    background-position: center;
  }
}
@media (min-width: 1900px) {
  .schoolCommunity-bg {
    background-size: unset;
    background-position: unset;
  }
}
@media (min-width: 1921px) {
  .schoolCommunity-bg {
    background-size: cover;
    background-position: center;
  }
}
</style>
