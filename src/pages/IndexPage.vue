<template>
  <q-page class="IndexPage max-w-screen-xl mx-auto">
    <div class="Banner bg-yellow-200 flex flex-col items-center justify-center">
      <BlogCard
        :title="blogData.title"
        :description="blogData.description"
        :tags="blogData.tags"
        mode="row"
      />
    </div>
  </q-page>
</template>

<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
});

const blogData = ref({
  title: "Where To Watch 'John Wick: Chapter 4'",
  description:
    "There's been no official announcement regarding John Wick: Chapter 4's streaming release. However, given it's a Lionsgate film, John Wick: Chapter 4 will eventually be released on Starz.Chapter 4 will eventually be released on Starz.Chapter 4 will eventually be released on Starz.Chapter 4 will eventually be released on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starzased on Starz.",
  tags: ['Movies', 'John Wick'],
});
</script>
