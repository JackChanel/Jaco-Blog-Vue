<template>
  <q-scroll-area class="fit bg-primary">
    <div class="w-full flex justify-between items-center px-4 py-4">
      <q-img class="w-1/4" :src="logo" />
      <q-icon class="cursor-pointer" name="menu" size="sm" />
    </div>
    <q-separator inset />

    <div class="p-2">
      <div
        :class="`m-1 p-2 cursor-pointer rounded-xl hover:bg-white ${activeItem === index ? 'bg-white' : ''}`"
        v-for="(item, index) in drawerItemList"
        :key="item.icon"
        @click="updateActiveItem(index)"
      >
        <q-icon :name="item.icon" size="sm" class="mr-3" color="grey-8" />
        <span>{{ item.title }}</span>
      </div>
    </div>
  </q-scroll-area>
</template>

<script lang="ts" setup>
import logo from 'assets/logo/jaco_logo_4.png';
const activeItem = ref(0);
const drawerItemList = [
  { icon: 'auto_awesome', title: '推荐' },
  { icon: 'book', title: '博客' },
  { icon: 'rocket_launch', title: '相关项目' },
  { icon: 'offline_bolt', title: '工具' },
];
function updateActiveItem(index: number) {
  activeItem.value = index;
}
</script>
