<template>
  <q-page class="IndexPage mx-auto xl:px-60 py-4 bg-gray-100">
    <div class="Banner">
      <BlogCard
        :title="blogData.title"
        :description="blogData.description"
        :tags="blogData.tags"
        mode="row"
      />
    </div>
    <main class="MainContainer grid gap-8 grid-cols-[minmax(0,1fr)_320px]">
      <div class="Content flex flex-col gap-4">
        <div class="ActiveBar flex items-center justify-between">
          <BaseTab :tab-list="tabList" />
          <a class="MoreLink flex items-center gap-2 cursor-pointer">
            <span>See all</span>
            <q-icon name="arrow_forward" />
          </a>
        </div>
        <div
          class="BlogCards grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-x-6 gap-y-16"
        >
          <BlogCard
            v-for="i in 5"
            :key="i"
            :title="blogData.title"
            :description="blogData.description"
            :tags="blogData.tags"
            mode="col"
          />
        </div>
      </div>
      <div class="Sidebar">
        <PersonalCard />
      </div>
    </main>
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

const tabList = ref([
  { title: 'Popular', icon: 'whatshot' },
  { title: 'Recent', content: 'Recent Content' },
  { title: 'Trending', content: 'Trending Content' },
]);
</script>
