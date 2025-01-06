<template>
  <div
    class="w-full overflow-hidden max-lg:max-w-[375px] max-lg:mx-auto"
  >
    <div class="w-full max-w-[1240px] mx-auto" v-if="courses.length > 0">
      <MoleculesWorkshop :workshop="courses[0]" />
      <MoleculesBeginners :workshop="courses[1]" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from "vue";
const courses = ref([]);

onMounted(async () => {
  try {
    const response = await fetch("/data/courses.json");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    const data = await response.json();
    courses.value = data;
  } catch (error) {
    console.error("Fetch error:", error);
  }
});
</script>
