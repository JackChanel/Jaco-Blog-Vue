<template>
  <q-page class="bg-primary">
    <header class="flex justify-between px-6">
      <BaseTabs />
      <div class="action-area flex items-center gap-6">
        <q-icon name="notifications" size="md"></q-icon>
        <q-icon name="light_mode" size="md"></q-icon>
        <SearchPopup />
      </div>
    </header>
    <q-separator />
    <main class="flex gap-8 mt-8 mx-8">
      <div class="grow">
        <MainCard />
      </div>
      <aside class="min-w-96">
        <PersonalCard />
      </aside>
    </main>
  </q-page>
</template>

<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
});
</script>
