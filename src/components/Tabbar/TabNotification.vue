<template>
  <div class="cursor-pointer relative">
    <q-icon name="o_notifications" class="text-gray-600 text-2xl"></q-icon>
    <div
      v-if="activeNotify"
      class="absolute top-0 right-0 w-2 h-2 bg-red-500 rounded-full flex items-center justify-center"
    ></div>
  </div>
</template>

<script lang="ts" setup>
const activeNotify = ref(true);
</script>
