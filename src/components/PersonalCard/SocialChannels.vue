<template>
  <div>
    <ul
      class="flex flex-row justify-evenly flex-wrap w-full py-4 px-2 text-center items-center"
    >
      <a
        v-for="channel in channelList"
        :key="channel.title"
        class="diamond-clip-path flex justify-center items-center w-10 h-10 bg-gray-500/30 cursor-pointer hover:bg-gray-500/50"
        :href="channel.link"
        target="_blank"
      >
        <SvgIcon :name="channel.icon" size="1.2rem" color="white" />
      </a>
    </ul>
  </div>
</template>

<script setup lang="ts">
const channelList = [
  {
    title: 'github',
    icon: 'github',
    link: 'https://github.com/JackChanel',
  },
  {
    title: 'csdn',
    icon: 'csdn',
    link: 'https://blog.csdn.net/HD_TMG',
  },
  {
    title: 'juejin',
    icon: 'juejin',
    link: 'https://juejin.com/',
  },
  {
    title: 'bili',
    icon: 'bili',
    link: 'https://bilibili.cn/',
  },
  {
    title: 'gitee',
    icon: 'gitee',
    link: 'https://gitee.com/',
  },
];
</script>

<style scoped lang="scss">
.diamond-clip-path {
  -webkit-clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
  clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
}
</style>
