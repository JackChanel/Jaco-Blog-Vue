<template>
  <div>
    <ul
      class="flex flex-row justify-evenly flex-wrap w-full py-4 px-2 text-center items-center"
    >
      <li v-for="id in 5" :key="id" class="diamond-clip-path bg-white">
        <SvgIcon name="github" size="1rem" color="grey" />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
.diamond-clip-path {
  -webkit-clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
  clip-path: polygon(50% 3%, 91% 25%, 91% 75%, 50% 97%, 9% 75%, 9% 25%);
  background: var(--background-trans);
}
</style>
