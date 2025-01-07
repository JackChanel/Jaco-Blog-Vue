<template>
  <svg
    aria-hidden="true"
    :fill="color"
    :style="'width:' + size + ';height:' + size"
  >
    <use :xlink:href="symbolId" />
  </svg>
</template>

<script lang="ts" setup>
import { computed } from 'vue';
const props = defineProps<{
  name: string;
  color?: string;
  size?: string;
}>();
const symbolId = computed(() => `#icon-${props.name}`);
</script>
