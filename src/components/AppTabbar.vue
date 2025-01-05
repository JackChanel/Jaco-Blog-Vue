<template>
  <div class="bg-white text-black w-screen flex justify-between">
    <div class="w-full flex flex-nowrap justify-between px-40">
      <div class="tabLeft flex items-center space-x-4">
        <figure class="my-2">
          <q-img class="w-16" :src="logo" />
        </figure>
        <div class="splitter h-5 w-[1px] bg-black"></div>
        <base-tabbar />
      </div>
      <div class="tabRight flex space-x-4 items-center">
        <q-btn class="bg-black text-white" label="Logout" icon="mdi-logout" />
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import logo from 'assets/logo/jaco_logo_4.png';
</script>
