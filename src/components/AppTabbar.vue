<template>
  <div class="bg-white text-black w-screen flex justify-between">
    <div class="w-full flex flex-nowrap justify-between px-40">
      <div class="tabLeft flex items-center space-x-5">
        <figure class="my-2">
          <q-img class="w-16" :src="logo" />
        </figure>
        <div class="splitter h-4 w-[2px] rounded-full bg-gray-500"></div>
        <BaseTabbar />
      </div>
      <div class="tabRight flex space-x-6 items-center">
        <TabNotification />
        <SearchBar />
        <UserMenu />
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import logo from 'assets/logo/jaco_logo_4.png';
</script>
