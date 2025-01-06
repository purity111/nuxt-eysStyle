<template>
  <!-- <div class="lg:px-[30px] lg:py-[20px]"> -->
  <div class="">
    <div
      @click="toggleChild"
      class="flex items-center justify-between py-[10px] px-[15px] lg:px-[30px] lg:py-[20px] border-b-[1px] border-[#DDDDDD]"
    >
      <h3 class="text-[14px] lg:text-[24px]">
        {{ props.child.title }}（<span class="inline-block text-[#FAB6B0]">{{
          props.child.contents.length
        }}</span
        >）
      </h3>

      <img
        :src="
          isExpanded
            ? '/img/common/minus-icon.svg'
            : '/img/common/plus-icon.svg'
        "
        class="w-[20px] lg:w-[40px]"
        alt="Toggle Icon"
      />
    </div>
    <div v-if="isExpanded">
      <ul
        v-if="props.child?.contents"
        class="flex flex-wrap justify-between lg:pt-[20px]"
      >
        <li
          v-for="(data, index) in props.child.contents"
          :key="index"
          class="w-[50%] lg:w-[32%] lg:mb-[20px]"
        >
          <AtomsAccordionItem
            :imgUrl="data.imgUrl"
            :title="data.title"
            :content="data.content"
            v-if="data"
          />
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps, ref } from "vue";

const props = defineProps<{
  child: any;
  isExpanded?: boolean;
}>();
const emit = defineEmits(["toggle-change"]);

const isExpanded = ref(props.isExpanded);

const toggleChild = () => {
  isExpanded.value = !isExpanded.value;
  emit("toggle-change", props.child.id);
};
</script>
