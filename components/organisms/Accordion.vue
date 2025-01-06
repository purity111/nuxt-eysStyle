<template>
  <div class="mt-[35px] lg:mt-[25px]">
    <div v-for="parent in props.parents" :key="parent.id" class="mb-[10px] lg:mb-[20px] border border-[#DDDDDD]">
      <div
        @click="toggleParent(parent.id)"
        class="flex items-center justify-between pl-[15px] pr-[10px] py-[15px] lg:px-[20px] lg:py-[30px] border-b-[1px] border-[#DDDDDD] bg-white border border-[#DDDDDD]"
      >
        <h3 class="text-[18px] lg:text-[28px]">
          {{ parent.title }}（<span class="inline-block text-[#FAB6B0]">{{
            getTotalContents(parent)
          }}</span
          >）
        </h3>
        <img
          :src="
            parentExpanded[parent.id]
              ? '/img/common/minus-icon.svg'
              : '/img/common/plus-icon.svg'
          "
          class="w-[30px] lg:w-[60px]"
          alt="Toggle Icon"
        />
      </div>
      <div v-if="parentExpanded[parent.id]">
        <AtomsChildAccordion
          v-for="child in parent.children"
          :key="child.id"
          :child="child"
          @toggle-change="handleChildToggle"
          :is-expanded="childExpanded[child.id]"
          class="border-b-[1px] border-[#DDDDDD] bg-white"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const props = defineProps<{ parents: Array<any> }>();
const parentExpanded = ref<{ [key: number]: boolean }>({});
const childExpanded = ref<{ [key: number]: boolean }>({});

const toggleParent = (id: number) => {
  parentExpanded.value[id] = !parentExpanded.value[id];
};

const handleChildToggle = (id: number) => {
  childExpanded.value[id] = !childExpanded.value[id];
};

const getTotalContents = (parent: any) => {
  return parent.children.reduce(
    (sum: number, child: any) => sum + child.contents.length,
    0
  );
};
</script>
