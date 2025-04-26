<template>
  <div class="bg-[#FFC107] lg:w-[484px] lg:h-[123px] rounded-[7px] flex flex-col justify-center">
    <p class="text-[#EEECEC] text-[14px] ml-5">{{ title }}</p>
    <p class="text-white text-[32px] ml-5">{{ totalNumber }}</p>
  </div>
</template>
<script setup>
const props = defineProps({
  title: String,
  totalNumber: String,
})
</script>
