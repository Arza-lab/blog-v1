<script setup>
const { data } = await useAsyncData('posts', () => queryContent('/').find())

definePageMeta({
  layout: 'home',
})
</script>

<template>
  <div>
    <LatestPost :post="data[0]" />
    <Suspense>
      <div class="flex-col flex-col items-center gap-3 p-4 py-20 px-10">
        <PostCard v-for="(post, index) in data" :key="post.title" :post="post" :index="index" />
      </div>
      <template #fallback>
        <div op50 italic>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
  </div>
</template>
