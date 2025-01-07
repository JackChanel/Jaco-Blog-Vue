<template>
  <div class="flex justify-evenly items-center w-full text-white">
    <div
      v-for="item in dataList"
      :key="item.title"
      class="flex flex-col items-center"
    >
      <span class="text-base font-bold">{{ item.value }}</span>
      <span class="text-white/80">{{ item.title }}</span>
    </div>
  </div>
</template>
<script setup lang="ts">
const dataList = ref([
  {
    title: '文字',
    value: '283K',
  },
  {
    title: '文章',
    value: '34',
  },
  {
    title: '分类',
    value: '14',
  },
  {
    title: '标签',
    value: '76',
  },
]);
</script>
<style lang="scss" scoped></style>
