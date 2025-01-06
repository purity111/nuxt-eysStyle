<template>
  <div class="school-slider">
    <div class="relative">
      <div class="school-swiper-button-prev">
        <img
          src="/img/common/arrow-l.png"
          class="w-[18px] lg:w-[38px]"
          alt="arrow"
        />
      </div>
      <div class="school-swiper-button-next">
        <img
          src="/img/common/arrow-r.png"
          alt="arrow"
          class="w-[18px] lg:w-[38px]"
        />
      </div>
      <Swiper
        :modules="[Navigation]"
        :navigation="{
          nextEl: '.school-swiper-button-next',
          prevEl: '.school-swiper-button-prev',
        }"
        :loop="true"
        :autoplay="true"
        :breakpoints="{
          300: {
            slidesPerView: 1.9,
            spaceBetween: 20,
          },
          1000: {
            slidesPerView: 4.7,
            spaceBetween: 20,
          },
        }"
        class="!ml-[20px] !lg:ml-[460px]"
      >
        <SwiperSlide v-for="(item, index) of datas" :key="index">
          <MoleculesSchoolSliderItem
            :titleEn="item?.titleEn"
            :titleJp="item?.titleJp"
            :imgUrl="item?.imgUrl"
            :logo="item?.logo"
            :schoolLink="item?.schoolLink"
            v-if="item"
          />
        </SwiperSlide>
      </Swiper>
    </div>
    <MoleculesLesson class="mt-[50px] lg:mt-[70px] lg:mt-[90px]" />
  </div>
</template>

<style scoped>
.school-slider .swiper {
  margin-left: 460px !important;
  padding-left: 0 !important;
}

.school-swiper-button-prev,
.school-swiper-button-next {
  width: 80px;
  height: 80px;
  position: absolute;
  transform: translateY(-50%);
  top: 50%;
  z-index: 10;
  display: grid;
  place-content: center;
  background-color: black;
  opacity: 0.5;
  cursor: pointer;
}

.school-swiper-button-prev {
  left: 340px;
}

.school-swiper-button-next {
  right: 340px;
}

@media (max-width: 450px) {
  .school-slider .swiper {
    margin-left: 20px !important;
  }

  .school-swiper-button-prev,
  .school-swiper-button-next {
    width: 40px;
    height: 40px;
  }

  .school-swiper-button-prev {
    left: 0;
  }

  .school-swiper-button-next {
    right: 0;
  }
}
</style>

<script setup lang="ts">
import { onMounted, ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper/modules";
import "swiper/swiper-bundle.css";

const datas = ref([]);
onMounted(async () => {
  try {
    const response = await fetch("/data/SchoolSlider.json");
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
