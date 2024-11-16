<template>
  <q-tabs v-model="currentTab" no-caps class="text-black">
    <q-tab name="mails" label="Mails" />
    <q-tab name="alarms" label="Alarms" />
    <q-tab name="movies" label="Movies" />
  </q-tabs>
</template>
<script lang="ts" setup>
const tabList = ['mails', 'alarms', 'movies'];
const currentTab = ref(tabList[0]);
</script>
