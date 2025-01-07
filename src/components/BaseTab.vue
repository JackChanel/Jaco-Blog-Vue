<template>
  <div>
    <div class="flex space-x-1 text-[13px] flex-wrap">
      <div
        v-for="(tab, index) in tabList"
        :key="tab.title"
        :class="[
          'flex gap-2 items-center px-3 py-[7px] h-[32px] rounded-lg border-[0.5px] font-medium leading-[18px] cursor-pointer    ',
          activeTab === index
            ? 'bg-white text-blue-500 shadow-xs'
            : 'text-gray-700 border-transparent hover:bg-gray-200',
        ]"
        @click="setActiveTab(index)"
      >
        <q-icon v-if="tab.icon" :name="tab.icon" />
        <span>{{ tab.title }}</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineOptions({
  name: 'BaseTab',
});
const props = defineProps<{
  tabList: { title: string; content?: string; icon?: string }[];
  defaultActive?: number;
}>();
const activeTab = ref(props.defaultActive || 0);
const setActiveTab = (index: number) => {
  activeTab.value = index;
};
</script>
