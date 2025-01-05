<template>
  <div class="Tabbar flex items-center">
    <a v-for="item in tabList" :key="item.label" :class="[`px-4`]"
      >{{ item.label }}
    </a>
  </div>
</template>
<script lang="ts" setup>
// const props = defineProps({});
const tabList = [
  {
    icon: 'home',
    label: '首页',
    path: '/',
  },
  {
    icon: 'blog',
    label: '博客',
    path: '/blog',
  },
  {
    icon: 'project',
    label: '项目',
    path: '/project',
  },
  {
    icon: 'activity',
    label: '隐藏',
    path: '/activity',
  },
];
</script>
