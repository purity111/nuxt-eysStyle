<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  course?: number[];
  cost?: number[];
}>();
</script>

<template>
  <table class="open-table hiragino-sans mb-[20px]">
    <thead class="bg-[#f9f9f9]">
      <tr class="text-[13px]">
        <th class="border-r-[1px] border-[#EEEEEE] font-normal">コース</th>
        <th style="text-align: right !important" class="!pr-[20px]">
          料金<span class="text-[10px] pl-[10px]">※ 制抜</span>
        </th>
      </tr>
    </thead>
    <tbody class="text-[11px]">
      <tr v-for="(value, index) in props.course" :key="index">
        <td class="w-[50%] border-r-[1px] border-[#EEEEEE] font-normal">
          {{ value }}回/月
        </td>
        <td class="w-[50%]">{{ cost[index] }}円</td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
.open-table {
  border-collapse: collapse;
  width: 100%;
}

.open-table th,
.open-table td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ccc;
}

td,
th {
  text-align: center !important;
}

tbody tr:last-of-type {
  border-bottom: none;
}
</style>
