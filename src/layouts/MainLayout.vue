<template>
  <q-layout view="lhr lpR lfr">
    <q-drawer show-if-above side="left" bordered>
      <DrawerContent />
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup></script>
