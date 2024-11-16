<template>
  <q-card class="bg-white rounded-xl">
    <q-card-section class="flex justify-between">
      <div class="flex flex-col gap-2">
        <div class="text-h6">I'm Jack Chanel</div>
        <span class="text-caption">
          Frontend Developer, Mini programs,
          <br />
          node server...
        </span>
        <div class="action">
          <button class="bg-black text-white p-1 px-2 rounded-md">
            <q-icon name="radio_button_checked" />
            Hire Me
          </button>
          <button
            class="bg-white rounded-md border-[0.5px] p-1 px-2 shadow-1 ml-4"
          >
            Copy Email
          </button>
        </div>
      </div>
      <q-avatar size="90px">
        <img :src="avatarImg" alt="avatar" />
      </q-avatar>
    </q-card-section>
    <q-card-section class="flex justify-between">
      <div class="flex items-center gap-4">
        <q-icon name="location_on" size="sm"></q-icon>
        <span class="text-caption">Hangzhou, China</span>
      </div>
    </q-card-section>
  </q-card>
</template>
<script lang="ts" setup>
import avatarImg from 'assets/avatar.png';
</script>
