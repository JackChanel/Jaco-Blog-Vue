<template>
  <div
    :class="[
      'CardWrapper flex flex-nowrap gap-10 p-4',
      `flex-${props.mode} text-sm`,
    ]"
  >
    <div class="Cover max-w-md">
      <img
        class="rounded-xl"
        src="https://jackchanel.oss-cn-hangzhou.aliyuncs.com/assets/cover.png"
        alt="Cover"
      />
    </div>
    <div
      :class="[
        'Content flex flex-col gap-3',
        props.mode === 'row' ? 'max-w-md' : '',
      ]"
    >
      <div class="UserInfo flex items-center gap-2 py-4">
        <q-avatar size="md">
          <img
            src="https://jackchanel.oss-cn-hangzhou.aliyuncs.com/assets/myavatar.png"
          />
        </q-avatar>
        <span>Jack Chanel</span>
        <span class="Dot w-[3px] h-[3px] rounded-full bg-black"></span>
        <span>2 days ago</span>
      </div>
      <span class="Title text-4xl">{{ props.title }}</span>
      <span class="Description line-clamp-3">{{ props.description }} </span>
      <div class="AppendInfo font-bold flex items-center gap-2">
        <span class="Tags text-red-500"> {{ props.tags.join(' ') }}</span>
        <span class="Dot w-[3px] h-[3px] rounded-full bg-black"></span>
        <span>4 min read</span>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
const props = defineProps<{
  title: string;
  description: string;
  tags: string[];
  mode: 'row' | 'col';
}>();
</script>
