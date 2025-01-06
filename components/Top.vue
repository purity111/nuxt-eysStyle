<template>
  <div class="relative">
    <OrganismsHeaderSection />
    <OrganismsEventCard :mon="1" :day="30" :price="2000" class="" />
    <OrganismsEventCardPc
      :mon="1"
      :day="30"
      :price="2000"
      class="mt-[-120px]"
    />
    <OrganismsAbout />
    <div
      class="bg-[url('/img/sp/school-community-sp.avif')] lg:bg-[url('/img/pc/school-community.avif')] schoolCommunity-bg"
    >
      <div class="relative z-20">
        <OrganismsSchool />
        <OrganismsAccordion
          :parents="accordionDatas"
          class="mt-[40px] mx-[10px] lg:m-auto lg:w-[1000px]"
        />
        <OrganismsSystem />
        <OrganismsCourse />
        <OrganismsCommunity />
      </div>
    </div>
    <OrganismsFooter />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";

const accordionDatas = ref([]);
onMounted(async () => {
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
