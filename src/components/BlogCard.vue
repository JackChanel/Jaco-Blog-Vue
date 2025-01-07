<template>
  <div
    :class="[
      'CardWrapper flex flex-nowrap  text-sm',
      props.mode === 'row' ? 'flex-row py-4 gap-14' : 'flex-col gap-4',
    ]"
  >
    <div :class="['Cover', props.mode === 'row' ? ' max-w-2xl' : '']">
      <img
        class="rounded-xl"
        src="https://jackchanel.oss-cn-hangzhou.aliyuncs.com/assets/cover.png"
        alt="Cover"
      />
    </div>
    <div
      :class="[
        'Content flex flex-col justify-around gap-3 text-base',
        props.mode === 'row' ? 'max-w-2xl' : '',
      ]"
    >
      <div class="ContentTop text-8xl font-bold" v-if="props.mode === 'row'">
        Top Article
      </div>
      <div class="ContentBottom flex flex-col gap-3">
        <div class="UserInfo flex items-center gap-2">
          <q-avatar :size="props.mode === 'row' ? 'md' : 'sm'">
            <img
              src="https://jackchanel.oss-cn-hangzhou.aliyuncs.com/assets/myavatar.png"
            />
          </q-avatar>
          <span>Jack Chanel</span>
          <span class="Dot w-[3px] h-[3px] rounded-full bg-black"></span>
          <span>2 days ago</span>
        </div>
        <span
          :class="[
            'Title font-bold',
            props.mode === 'row' ? 'text-3xl' : 'text-xl',
          ]"
          >{{ props.title }}</span
        >
        <span class="Description line-clamp-3">{{ props.description }} </span>
        <div class="AppendInfo font-bold flex items-center gap-2">
          <span class="Tags text-red-500"> {{ props.tags.join(' ') }}</span>
          <span class="Dot w-[3px] h-[3px] rounded-full bg-black"></span>
          <span>4 min read</span>
        </div>
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
